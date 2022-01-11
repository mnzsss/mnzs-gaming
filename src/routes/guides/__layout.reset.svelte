<script>
	import '../../styles/global.css';

	import { APP_NAME } from '../../utils/constants';
	import Title from '$lib/title.svelte';

	export let pageTitle = '';

	let footerTitle = pageTitle ? `${APP_NAME} ${pageTitle}` : APP_NAME;
</script>

<header>
	<nav>
		<Title page={pageTitle} />
		<div class="links">
			<a href="/">Home</a>
			<a href="/about">About</a>
			<a href="/guides">Guides</a>
		</div>
	</nav>
</header>

<main>
	<!-- Page Content -->
	<!-- Slot Tag mark in html template where the children will rendered -->
	<slot />
</main>

<footer>
	<p>Copyright 2022 {footerTitle}</p>
</footer>

<style>
	header {
		text-align: center;
		background: rgba(0, 0, 0, 0.1);
	}
	main {
		max-width: 960px;
		margin: 20px auto;
	}
	footer {
		text-align: center;
	}
	.links {
		margin-left: auto;
	}
	a {
		margin-left: 10px;
	}
	nav {
		display: flex;
		align-items: center;
		max-width: 960px;
		margin: 0 auto;
	}
</style>
