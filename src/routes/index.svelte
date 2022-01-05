<script>
	const DEFAULT_TITLE = 'Menezes Gaming guides';
	let title = DEFAULT_TITLE;

	const resetTitle = () => {
		title = DEFAULT_TITLE;
	};
</script>

<div class="index">
	<h2>{title}</h2>
	<p>
		Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum beatae perferendis fugiat dolor
		deserunt in ad sit ipsa possimus exercitationem?
	</p>

	<button on:click={resetTitle}>Reset Title </button>
	<input type="text" bind:value={title} name="title" />
</div>

<style>
	.index {
		text-align: center;
		display: block;
		margin: 20px auto;
	}
</style>
