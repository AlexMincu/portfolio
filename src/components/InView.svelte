<script>
	// @ts-nocheck

	/* Docs:
        https://github.com/the-pudding/the-svelte-way/blob/main/src/components/episodes/e3/InView.svelte
        https://blog.arnellebalane.com/the-intersection-observer-api-d441be0b088d 
    */
	import { onMount } from 'svelte';

	let isVisible = false;
	export let card = false;
	let element;

	const handleIntersect = (e) => {
		isVisible = e[0].isIntersecting;
	};

	onMount(() => {
		const root = null;
		const rootMargin = `0px 0px -50px 0px`;
		const options = { root, rootMargin };

		const observer = new IntersectionObserver(handleIntersect, options);
		observer.observe(element);
	});
</script>

<div bind:this={element}>
	<div
		class:isVisible
		class="opacity-0 transition duration-[800ms] ease-in-out {card ? '-translate-x-[100vw]' : ''}"
	>
		<slot />
	</div>
</div>

<style>
	.isVisible {
		@apply translate-x-0 opacity-100;
	}
</style>
