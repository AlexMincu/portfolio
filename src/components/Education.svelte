<script>
	import InView from './InView.svelte';
	import Border from './Border.svelte';
</script>

<InView let:isVisible>
	<div class="relative mb-[40vh] mt-[20vh] px-[5vh] py-[10vh]">
		<Border {isVisible} />

		<h2 class="mb-2 text-center text-5xl uppercase tracking-widest opacity-40">Education</h2>

		<div class="md:mx-10 md:grid md:grid-cols-[80%_20%]">
			<div class="text-lg font-light">Computers and Information Technology</div>
			<div class="text-end text-sm italic">Bucharest, RO</div>
			<div class="font-bold">University of Bucharest</div>
			<div class="text-end text-sm italic">2019 - 2023</div>
		</div>
	</div>
</InView>
