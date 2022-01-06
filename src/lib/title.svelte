<script>
	export let title = 'Menezes Gaming';
	export let page = '';

	const fTitle = page ? `${title} | ${page}` : title;
</script>

<div class="title">
	<img src="/controller.svg" alt="MNZS Gaming Logo" />
	<h1>{fTitle}</h1>
</div>

<style>
	.title {
		display: flex;
		align-items: center;
	}

	.title img {
		display: inline-block;
		filter: invert(88%) sepia(18%) saturate(886%) hue-rotate(199deg) brightness(100%) contrast(90%);
	}
	.title h1 {
		margin-left: 10px;
	}
</style>
