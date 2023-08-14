<script>
	import InView from './InView.svelte';
	import Border from './Border.svelte';

	let innerWidth = 0;

	$: isMobileWidth = innerWidth < 768;
</script>

<svelte:window bind:innerWidth />

<InView let:isVisible>
	<div class="relative mt-[20vh] px-[5vh] py-[10vh] md:mb-[40vh]">
		<Border {isVisible} />

		<h2 class="mb-8 text-center text-5xl uppercase tracking-widest opacity-40">Education</h2>

		{#if isMobileWidth}
			<div class="">
				<div class="text-center text-xl font-light">Computers and Information Technology</div>
				<div class="text-center text-lg font-bold">University of Bucharest</div>
				<div class="text-md text-center italic">Bucharest, RO</div>
				<div class="text-md text-center italic">2019 - 2023</div>
			</div>
		{:else}
			<div class="mx-10 grid grid-cols-[80%_20%]">
				<div class="text-xl font-light">Computers and Information Technology</div>
				<div class="text-md text-end italic">Bucharest, RO</div>
				<div class="text-lg font-bold">University of Bucharest</div>
				<div class="text-md text-end italic">2019 - 2023</div>
			</div>
		{/if}
	</div>
</InView>
