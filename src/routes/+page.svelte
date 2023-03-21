<script>
	import { onMount } from 'svelte';
	import { el } from '@elemaudio/core';
	import { default as core } from '@elemaudio/plugin-renderer';


	core.on('load', () => {

		let left_in = el.in({ channel: 0 });
		let right_in = el.in({ channel: 1 });

		core.render(left_in, right_in);
	});

	onMount(() => {
		core.initialize();
	});
</script>

<main>
	<h1>Hello world!</h1>
</main>
	
<style>
	main {
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>