<script>
	import './modal.css';
	import './font-settings.css';
	import './grid.css';
	import HeadComponent from '$lib/HeadComponent.svelte';
	import GitHubIcon from '$lib/icons/fontawesome/github.svelte';
	const DOWNLOAD_BASE = 'https://github.com/mistweaverco/bananas/releases/latest/download/';

	/**
	 * @type {boolean}
	 */
	let modalLinuxDownloadIsActive = false;

	const toggleModalLinuxDownload = () => {
		modalLinuxDownloadIsActive = !modalLinuxDownloadIsActive;
	};
	/**
	 * @param {MouseEvent} evt
	 * @this {HTMLAnchorElement}
	 */
	function showFullScreenImage(evt) {
		evt.preventDefault();
		const img = /** @type {HTMLImageElement} */ (this.querySelector('img'));
		img.requestFullscreen();
	}
</script>

<HeadComponent
	data={{
		title: 'Bananas Screen Sharing',
		description:
			'Bananas, cross-platform, p2p screen sharing made simple. Share your screen with anyone, anywhere, anytime.'
	}}
/>

<div class="modal {modalLinuxDownloadIsActive ? 'is-active' : ''}">
	<div class="modal-background"></div>
	<div class="modal-content">
		<button on:click={toggleModalLinuxDownload} class="modal-close is-large" aria-label="close">
			<span aria-hidden="true">&times;</span>
		</button>
		<div class="box">
			<button class="button is-debian">
				<a href="{DOWNLOAD_BASE}bananas_amd64.deb">
					<span class="icon">
						<i class="fa-brands fa-debian"></i>
					</span>
					<span>.deb</span>
				</a>
			</button>
			<button class="button is-snap">
				<a href="{DOWNLOAD_BASE}bananas_amd64.snap">
					<span class="icon">
						<i class="fa-brands fa-linux"></i>
					</span>
					<span>.snap</span>
				</a>
			</button>
			<button class="button is-appimage">
				<a href="{DOWNLOAD_BASE}bananas_x86_64.AppImage">
					<span class="icon">
						<i class="fa-solid fa-cube"></i>
					</span>
					<span>.AppImage</span>
				</a>
			</button>
		</div>
	</div>
</div>

<div class="container is-intro">
	<div class="inner">
		<img src="/logo.svg" alt="Bananas logo" />
		<header>Bananas Screen Sharing</header>
		<a href="https://github.com/mistweaverco/bananas/releases/latest">
			<img
				src="https://img.shields.io/github/v/release/mistweaverco/bananas?style=for-the-badge"
				alt="Download latest release"
			/>
		</a>
		<a href="https://github.com/mistweaverco/bananas">
			<img
				src="https://img.shields.io/github/downloads/mistweaverco/bananas/total.svg?style=for-the-badge"
				alt="Downloads counter"
			/>
		</a>
		<a href="https://typescriptlang.org">
			<img src="/badge-typescript.svg" alt="Made with TypeScript" />
		</a>
		<a href="https://electronjs.org">
			<img src="/badge-electron.svg" alt="Powered by Electron" />
		</a>
		<a href="https://v2.vitejs.dev">
			<img src="/badge-vite.svg" alt="Powered by Vite" />
		</a>
		<a href="https://discord.gg/BeN43eJVWS">
			<img src="/badge-discord.svg" alt="Join our Discord" />
		</a>
		<p>Bananas 🍌, cross-platform, p2p screen 🖥️ sharing 📡 made simple ⚡.</p>
		<div class="see-the-source">
			<div class="download-buttons">
				<button class="button is-windows">
					<a href="{DOWNLOAD_BASE}bananas-setup_x64.exe">
						<span class="icon">
							<i class="fa-brands fa-windows"></i>
						</span>
						<span>Windows</span>
					</a>
				</button>
				<button class="button is-mac">
					<a href="{DOWNLOAD_BASE}bananas_universal.dmg">
						<span class="icon">
							<i class="fa-brands fa-apple"></i>
						</span>
						<span>Mac</span>
					</a>
				</button>
				<button on:click={toggleModalLinuxDownload} class="button is-linux">
					<span class="icon">
						<i class="fa-brands fa-linux"></i>
					</span>
					<span>Linux</span>
				</button>
			</div>
			<a
				href="https://github.com/mistweaverco/bananas"
				title="Check out the source code on GitHub"
				class="github-icon"
			>
				<GitHubIcon />
			</a>
		</div>
	</div>
</div>
<div class="container is-more">
	<div class="inner">
		<div class="grid has-3-cols">
			<div class="item">
				<h2>Multiple cursors 🖱️</h2>
				<p>
					Share your screen 🖥️ with anyone 🌈, anywhere 🏝️, anytime 🕗 and collaborate with multiple
					cursors.
				</p>
				<a
					href="/showcase-multiple-cursors.png"
					on:click={showFullScreenImage}
					target="_blank"
					rel="noopener"
				>
					<img
						src="/showcase-multiple-cursors.png"
						class="rounded"
						alt="Multiple cursors showcase"
					/>
				</a>
				<p>
					Utilize the awesome Bananas 🍌 ping feature ✨ where you can mark important 🚨 areas with
					your remote cursor.
				</p>
			</div>
			<div class="item">
				<h2>Zero configuration 🚫</h2>
				<p>
					No need to sign up, log in, or create an account 🥷. Just share your screen and start
					collaborating.
				</p>
				<p>
					Bananas 🍌 creates a unique 🌟 connection url 🌐 for you to share with your friends,
					family, or colleagues.
				</p>
				<p>
					These urls should be treated as <strong>sensitive</strong> information.
				</p>
				<p>
					Because there are no servers involved (except for the stun, turn and signaling servers
					that are needed for exchanging the initial connection information), you need to have a way
					to communicate the url to the person you're sharing your screen with.
				</p>
			</div>
			<div class="item">
				<h2>Privacy first 🕵️</h2>
				<p>
					Your data is
					<a href="https://github.com/mistweaverco/bananas?tab=readme-ov-file#1-data-collection">
						never stored
					</a> on any server. It's a direct connection between you and the person you're sharing your
					screen with.
				</p>
				<a
					href="/webrtc-flowchart.png"
					on:click={showFullScreenImage}
					target="_blank"
					rel="noopener"
				>
					<img src="/webrtc-flowchart.png" class="rounded" alt="Multiple cursors showcase" />
				</a>
				<p>
					We use <a href="https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API">WebRTC</a> technology
					to establish a secure connection between you and the person you're sharing your screen with.
				</p>
			</div>
		</div>
	</div>
</div>
