<script>
	import InView from './InView.svelte';
	import Border from './Border.svelte';
</script>

<InView let:isVisible>
	<div class="relative mb-[40vh] mt-[20vh] px-[5vh] py-[10vh]">
		<Border {isVisible} />

		<h2 class="mb-8 text-center text-5xl uppercase tracking-widest opacity-40">Education</h2>

		<div class="md:mx-10 md:grid md:grid-cols-[80%_20%]">
			<div class="text-xl font-light">Computers and Information Technology</div>
			<div class="text-md text-end italic">Bucharest, RO</div>
			<div class="text-lg font-bold">University of Bucharest</div>
			<div class="text-md text-end italic">2019 - 2023</div>
		</div>
	</div>
</InView>
