<script>
	import InView from '../components/InView.svelte';
	import Tesseract from './Tesseract.svelte';
</script>

<div
	class="flex h-screen w-full flex-col items-center justify-center overflow-hidden text-center md:flex-row md:overflow-visible"
>
	<InView>
		<div class="-translate-x-26 h-[300px] w-[300px] scale-75">
			<Tesseract />
		</div>
	</InView>

	<div class="h-fit">
		<InView>
			<h1 class="mb-2 font-mono text-6xl">Minculescu <span class="font-bold">Alexandru</span></h1>
		</InView>

		<InView>
			<h2 class="mb-3 text-2xl">Software Engineer</h2>
		</InView>
	</div>
</div>
