<script>
	import './modal.css';
	import './font-settings.css';
	import './grid.css';
	import HeadComponent from '$lib/HeadComponent.svelte';
</script>

<HeadComponent
	data={{
		title: 'Bananas Screen Sharing - Tutorial',
		description:
			'A quick tutorial on how to use Bananas Screen Sharing. Share your screen with anyone, anywhere, anytime and collaborate with multiple cursors.',
	}}
/>

<div class="container is-intro">
	<div class="inner">
		<img src="/logo.svg" alt="Bananas logo" />
		<header>Bananas Screen Sharing - Tutorial</header>
		<p>
			This tutorial will guide you through the process of sharing your screen with Bananas Screen Sharing.
		</p>
	</div>
</div>

<div class="container is-more">
	<div class="inner">
		<div class="grid has-3-cols">
			<div class="item">
				<h2>1. Host: Host a session</h2>
				<p>
					Click on host a session to start sharing your screen.
				</p>
				<a
					href="/tutorial/001-click-host-a-session.png"
					target="_blank"
					rel="noopener"
				>
					<img
						src="/tutorial/001-click-host-a-session.png"
						class="rounded"
						alt="Click on host a session"
					/>
				</a>
			</div>
			<div class="item">
				<h2>2. Host: Click start a new session</h2>
				<p>
					You'll be given a unique url that you can share with your friends, family, or colleagues.
				</p>
				<a
					href="/tutorial/002-click-start-a-new-session.png"
					target="_blank"
					rel="noopener"
				>
					<img
						src="/tutorial/002-click-start-a-new-session.png"
						class="rounded"
						alt="Click start a new session"
					/>
				</a>
			</div>
			<div class="item">
				<h2>3. Host: Optionally select a screen to share</h2>
				<p>
					If you have multiple screens,
					you can select the one you want to share.
				</p>
				<a
					href="/tutorial/003-optionally-select-a-screen-to-share.png"
					target="_blank"
					rel="noopener"
				>
					<img src="/tutorial/003-optionally-select-a-screen-to-share.png" class="rounded" alt="select a screen to share" />
				</a>
			</div>
			<div class="item">
				<h2>4. Host: Copy host connection string</h2>
				<p>
					Click on the copy button to copy the host connection string.
				</p>
				<a
					href="/tutorial/004-click-copy-my-connection-string.png"
					target="_blank"
					rel="noopener"
				>
					<img src="/tutorial/004-click-copy-my-connection-string.png" class="rounded" alt="copy host connection string" />
				</a>
			</div>
			<div class="item">
				<h2>5. Host: Send link to participant</h2>
				<p>
					Send the copied host connection string to the participant.
				</p>
				<a
					href="/tutorial/005-send-the-host-link-to-the-participant.png"
					target="_blank"
					rel="noopener"
				>
					<img src="/tutorial/005-send-the-host-link-to-the-participant.png" class="rounded" alt="send host connection string to participant" />
				</a>
			</div>
			<div class="item">
				<h2>6. Participant: Join session</h2>
				<p>
					Joined the session by clicking on the link,
					or by pasting it into the host connection string input field and click connect.
				</p>
				<a
					href="/tutorial/006-join-session-by-pasting-host-link-in-field-and-click-connect.png"
					target="_blank"
					rel="noopener"
				>
					<img src="/tutorial/006-join-session-by-pasting-host-link-in-field-and-click-connect.png" class="rounded" alt="join host" />
				</a>
			</div>
			<div class="item">
				<h2>7. Participant: Copy connection string</h2>
				<p>
					Click on the copy button to copy the participant connection string.
				</p>
				<a
					href="/tutorial/007-participant-click-on-copy-my-connection-string.png"
					target="_blank"
					rel="noopener"
				>
					<img src="/tutorial/007-participant-click-on-copy-my-connection-string.png" class="rounded" alt="copy connection string" />
				</a>
			</div>
			<div class="item">
				<h2>8. Participant: Send URL to host</h2>
				<p>
					Send the copied participant connection string to the host.
				</p>
				<a
					href="/tutorial/008-participant-send-url-to-host.png"
					target="_blank"
					rel="noopener"
				>
					<img src="/tutorial/008-participant-send-url-to-host.png" class="rounded" alt="copy connection string" />
				</a>
			</div>
			<div class="item">
				<h2>9. Host: paste participant URL</h2>
				<p>
					Paste the participant connection string into the input field and click connect.
				</p>
				<a
					href="/tutorial/009-host-paste-participant-url-in-field-and-click-connect.png"
					target="_blank"
					rel="noopener"
				>
					<img src="/tutorial/009-host-paste-participant-url-in-field-and-click-connect.png" class="rounded" alt="paste participant url and click connect" />
				</a>
			</div>
			<div class="item">
				<h2>10. Participant: streaming starts</h2>
				<p>
					You'll see the host's screen and cursor.
				</p>
				<a
					href="/tutorial/010-participant-streaming-starts.png"
					target="_blank"
					rel="noopener"
				>
					<img src="/tutorial/010-participant-streaming-starts.png" class="rounded" alt="streaming starts" />
				</a>
			</div>
			<div class="item">
				<h2>11. Host: controls</h2>
				<p>
					Host can control the session by clicking on the buttons.
				</p>
				<p>
					Host can e.g. enable or disable the participant's cursor on his screen.
				</p>
				<a
					href="/tutorial/011-host-controls.png"
					target="_blank"
					rel="noopener"
				>
					<img src="/tutorial/011-host-controls.png" class="rounded" alt="host controls" />
				</a>
			</div>
		</div>
	</div>
</div>
