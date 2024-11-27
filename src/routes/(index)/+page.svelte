<script>
	import './modal.css';
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

<div class="container">
	<div class="inner">
		<img src="/logo.svg" alt="Bananas logo" />
		<header>Bananas Screen Sharing</header>
		<a href="https://github.com/mistweaverco/bananas/releases/latest">
			<img
				src="https://img.shields.io/github/v/release/mistweaverco/bananas?style=for-the-badge"
				alt="Download latest release"
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
			<img src="/showcase-multiple-cursors.png" class="rounded" alt="Multiple cursors showcase" />
		</a>
		<p>
			Utilize the awesome Bananas 🍌 ping feature ✨ where you can mark important 🚨 areas with your
			remote cursor.
		</p>
		<h2>Zero configuration 🚫</h2>
		<p>
			No need to sign up, log in, or create an account 🥷. Just share your screen and start
			collaborating.
		</p>
		<h2>Privacy first 🕵️</h2>
		<p>
			Your data is never stored on any server. It's a direct connection between you and the person
			you're sharing your screen with.
		</p>
	</div>
</div>

<style>
	button.button {
		padding: 0.2rem 0.5rem;
		font-size: 0.8rem;
		border-radius: 5px;
		border: 0 none;
		cursor: pointer;
	}
	.button.is-windows {
		background-color: #0078d4;
		color: #fff;
	}
	.button.is-mac {
		background-color: #000;
		color: #fff;
	}
	.button.is-debian {
		background-color: #a80030;
		color: #fff;
	}
	.button.is-linux {
		background-color: #dd4814;
		color: #fff;
	}
	.button.is-snap {
		background-color: #dd4814;
		color: #fff;
	}
	.button.is-appimage {
		background-color: #4e9a06;
		color: #fff;
	}
	.container {
		text-align: center;
		font-size: 1.5rem;
	}

	img.rounded {
		border-radius: 20px;
	}

	.download-buttons {
		display: flex;
		justify-content: center;
		margin-bottom: 1rem;
	}

	.download-buttons button {
		margin: 0 0.2rem;
	}

	button a {
		color: #fff;
		text-decoration: none;
	}

	header,
	p {
		font-family: 'Indie Flower', cursive;
	}

	header {
		font-size: 2rem;
	}

	h2 {
		font-size: 1.3rem;
	}

	p {
		font-size: 1.2rem;
	}

	.inner {
		text-align: center;
		width: 85%;
		margin: auto;
		min-height: calc(100vh - 4rem);
		font-family: monospace;
		max-width: 530px;
	}

	.see-the-source {
		padding-bottom: 3rem;
		margin-bottom: 3rem;
		border-bottom: 1px solid #333;
	}

	.see-the-source a {
		color: #fff;
		text-decoration: none;
		border: 0 none;
	}

	.github-icon :global(svg):hover {
		fill: #ff6480;
	}

	.github-icon :global(svg) {
		transition: fill 0.5s;
		display: inline-block;
		cursor: pointer;
		height: 32px;
		width: 32px;
	}

	img {
		max-width: 100%;
	}
	.modal .box button {
		margin: 0 0.2rem;
	}
</style>
