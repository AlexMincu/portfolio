<script>
	import InView from './InView.svelte';
	import Border from './Border.svelte';

	let innerWidth = 0;

	$: isMobileWidth = innerWidth < 768;
</script>

<svelte:window bind:innerWidth />

<InView let:isVisible>
	<div class="relative mt-[20vh] px-[5vh] py-[10vh] md:mb-[40vh] md:mt-[70vh]">
		<Border {isVisible} />

		<h2 class="mb-4 text-center text-4xl uppercase tracking-widest opacity-40 md:text-5xl">
			Experience
		</h2>

		<div class="flex flex-col gap-6 md:mx-8">
			<div>
				{#if isMobileWidth}
					<div class="">
						<div class="text-center text-lg font-light uppercase tracking-wide">PR Assistant</div>
						<div class="text-center font-semibold">HKR Media SRL</div>
						<div class="text-center text-sm italic">Bucharest, RO</div>
						<div class="mt-2 text-center text-sm italic">Nov 2022 - Jan 2023</div>
						<div class="text-center text-sm italic">Nov 2021 - Dec 2021</div>
					</div>
				{:else}
					<div class="grid grid-cols-2">
						<div class="text-lg font-light uppercase tracking-wide">PR Assistant</div>
						<div class="text-end text-sm italic">Bucharest, RO</div>
						<div class="font-semibold">HKR Media SRL</div>
						<div class="text-end text-sm italic">Nov 2022 - Jan 2023</div>
						<div />
						<div class="text-end text-sm italic">Nov 2021 - Dec 2021</div>
					</div>
				{/if}

				<div class="mt-4 text-justify">
					I worked as a Public Relations Assistant where I helped the clients of a designated
					company, provided by HKR Media. Learned the internal rules and responsibilities, and
					developed my ability to communicate and empathize with people in need. This experience
					helped a lot in my personal development as I had to be ready at all times to give a good
					response through email and reliably solve people's problems.
				</div>
			</div>

			<div>
				{#if isMobileWidth}
					<div class="">
						<div class="text-center text-lg font-light uppercase tracking-wide">QA Tester</div>
						<div class="text-center font-semibold">Electronic Arts</div>
						<div class="text-center text-sm italic">Bucharest, RO</div>
						<div class="mt-2 text-center text-sm italic">Jul 2020 - Oct 2020</div>
					</div>
				{:else}
					<div class="grid grid-cols-2">
						<div class="text-lg font-light uppercase tracking-wide">QA Tester</div>
						<div class="text-end text-sm italic">Bucharest, RO</div>
						<div class="font-semibold">Electronic Arts</div>
						<div class="text-end text-sm italic">Jul 2020 - Oct 2020</div>
					</div>
				{/if}

				<div class="mt-2 text-justify md:mt-4">
					I worked as a quality assurance tester for games provided by Electronic Arts. I learned
					the procedures of testing bugs by analyzing and evaluating test cases. I was responsible
					for documenting and adding the bugs I found to Jira; provide logs, media files, and the
					steps to reproduce them.
				</div>
			</div>
		</div>
	</div>
</InView>
