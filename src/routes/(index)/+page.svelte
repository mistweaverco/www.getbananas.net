<script>
	import HeadComponent from '$lib/HeadComponent.svelte';
	import GitHubIcon from '$lib/icons/fontawesome/github.svelte';
</script>

<HeadComponent
	data={{
		title: 'Bananas Screen Sharing',
		description:
			'Bananas, cross-platform, p2p screen sharing made simple. Share your screen with anyone, anywhere, anytime.'
	}}
/>

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
			<a
				href="https://github.com/mistweaverco/bananas"
				title="Check out the source code on GitHub"
				class="github-icon"
			>
				<GitHubIcon />
			</a>
		</div>
		<h2>Multiple cursors 🖱️</h2>
		<p>Share your screen with anyone, anywhere, anytime and collaborate with multiple cursors.</p>
		<img src="/showcase-multiple-cursors.jpg" class="rounded" alt="Multiple cursors showcase" />
		<h2>Zero configuration 🚫</h2>
		<p>
			No need to sign up, log in, or create an account. Just share your screen and start
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
	.container {
		margin: 0;
		padding: 0;
		width: 100%;
		height: auto;
		min-height: 100vh;
		text-align: center;
		position: relative;
		font-size: 1.5rem;
		color: #fff;
		background-color: #1b1b1b;
	}

	img.rounded {
		border-radius: 20px;
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
</style>
