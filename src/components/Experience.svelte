<script>
	import InView from './InView.svelte';
</script>

<div class="mb-24">
	<InView>
		<h2 class="mb-4 text-center text-5xl uppercase tracking-widest opacity-40">Experience</h2>
	</InView>

	<div class="mx-8 flex flex-col gap-6">
		<InView>
			<div>
				<div class="grid grid-cols-2">
					<div class="text-lg font-light uppercase tracking-wide">PR Assistant</div>
					<div class="text-end text-sm italic">Bucharest, RO</div>
					<div class="font-semibold">HKR Media SRL</div>
					<div class="text-end text-sm italic">Nov 2022 - Jan 2023</div>
					<div />
					<div class="text-end text-sm italic">Nov 2021 - Dec 2021</div>
				</div>

				<div class="mt-4 text-justify">
					I worked as a Public Relations Assistant where I helped the clients of a designated
					company, provided by HKR Media. Learned the internal rules and responsibilities, and
					developed my ability to communicate and empathize with people in need. This experience
					helped a lot in my personal development as I had to be ready at all times to give a good
					response through email and reliably solve people's problems.
				</div>
			</div>
		</InView>

		<InView>
			<div>
				<div class="grid grid-cols-2">
					<div class="text-lg font-light uppercase tracking-wide">QA Tester</div>
					<div class="text-end text-sm italic">Bucharest, RO</div>
					<div class="font-semibold">Electronic Arts</div>
					<div class="text-end text-sm italic">Jul 2020 - Oct 2020</div>
				</div>

				<div class="mt-4 text-justify">
					I worked for a couple of months as a quality assurance tester for games provided by
					Electronic Arts. I learned the procedures of testing bugs by analyzing and evaluating test
					cases. I had to document and add the bugs found into the tracking bugs software; provide
					logs, media files, and other information on how to reproduce them.
				</div>
			</div>
		</InView>
	</div>
</div>
