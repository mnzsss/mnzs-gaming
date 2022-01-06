<script>
	import '../styles/global.css';

	import { APP_NAME } from '../utils/constants';
	import Title from '$lib/title.svelte';

	export let pageTitle = '';

	let footerTitle = pageTitle ? `${APP_NAME} ${pageTitle}` : APP_NAME;
</script>

<header>
	<Title page={pageTitle} />
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
		display: flex;
		justify-content: center;
		margin-top: 60px;
	}
	main {
		max-width: 960px;
		margin: 20px auto;
	}
	footer {
		text-align: center;
	}
</style>
