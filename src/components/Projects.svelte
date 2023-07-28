<script>
	// @ts-nocheck

	import ProjectsItem from './ProjectsItem.svelte';
	import InView from './InView.svelte';

	const projects = [
		{
			image_url: '/projects/championsfood.jpg',
			title: "Champion's Food",
			description:
				'A Windows application that simulates a Food Delivery service. It contains 7 different pages as well as automatically generated pages for every restaurant. Built using Java SE 15, utilizing Swing and SQL for a relational database.',
			links: [
				{
					title: 'Github',
					url: 'https://github.com/AlexMincu/FoodDeliveryApp'
				}
			],
			technologies: ['Java', 'Swing', 'MVC', 'SQL']
		},

		{
			image_url: '/projects/arcanearts.png',
			title: 'Arcane Arts',
			description:
				'A simple idle/clicker game made in C++ using the SFML library. The game is made from scratch, including the game engine. This is the first game I developed. It helped me understand how object-oriented programming works and how a more complex game would work.',
			links: [
				{
					title: 'Github',
					url: 'https://github.com/AlexMincu/ArcaneArts'
				}
			],
			technologies: ['C++', 'OOP', 'SFML']
		}
	];
</script>

<div class="mb-24">
	<InView>
		<h2
			class="mx-auto mb-2 min-w-0 max-w-[48rem] text-center text-5xl uppercase tracking-widest opacity-40"
		>
			Projects
		</h2>
	</InView>

	<!-- Main projects -->
	<div class="my-16">
		<!-- MyFitnessLog -->
		<InView>
			<div class="mx-auto mb-16 grid h-[600px] w-full grid-cols-[45%_55%] xl:w-[1280px]">
				<div class="mb-20 flex flex-col justify-center gap-4 pr-16 text-center align-middle">
					<div class="text-2xl uppercase tracking-wide">MyFitnessLog</div>
					<div class="mb-2 text-justify text-stone-600">
						MyFitnessLog is a fitness tracking web app designed to help users monitor their training
						routines. It was developed using modern technologies and cloud services - Supabase,
						Vercel
					</div>

					<div class="mb-2 flex flex-row flex-wrap justify-center gap-2 align-middle">
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">SvelteKit</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">SkeletonUI</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">
							TailwindCSS
						</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">PostgreSQL</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">Prisma</div>
					</div>

					<div class="flex flex-row justify-center gap-3 align-middle">
						<button
							class="block rounded-xl bg-blue-700 px-6 py-3 font-bold text-white shadow-2xl hover:bg-blue-600"
							target="_blank"
							href="https://myfitnesslog.vercel.app/">Website</button
						>

						<a
							class="block rounded-xl bg-blue-700 px-6 py-3 font-bold text-white shadow-2xl hover:bg-blue-600"
							target="_blank"
							href="https://github.com/AlexMincu/MyFitnessLog">Github</a
						>
					</div>
				</div>

				<div class="relative">
					<img
						class="absolute right-[15px] top-[50%] h-[80%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/myfitnesslog/myfitnesslog_tablet_preview.png"
						alt=""
					/>

					<img
						class="absolute left-[5%] top-[40%] h-[70%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/myfitnesslog/myfitnesslog_mobile_hero.png"
						alt=""
					/>
					<img
						class="absolute left-0 top-[60%] h-[70%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/myfitnesslog/myfitnesslog_mobile_preview.png"
						alt=""
					/>
				</div>
			</div>
		</InView>

		<!-- Ebisu -->
		<InView>
			<div class="mx-auto grid h-[600px] w-full grid-cols-[55%_45%] xl:w-[1280px]">
				<div class="relative">
					<img
						class="absolute right-0 top-[40%] h-[75%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/ebisu/ebisu_desktop_preview.png"
						alt=""
					/>

					<img
						class="absolute left-0 top-[55%] h-[85%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/ebisu/ebisu_mobile_preview.png"
						alt=""
					/>
				</div>

				<div class="mb-20 flex flex-col justify-center gap-4 pl-16 text-center align-middle">
					<div class="text-2xl uppercase tracking-wide">Ebisu</div>
					<div class="mb-2 text-justify text-stone-600">
						A fictional responsive eCommerce website. Used HTML, SCSS, and modern JavaScript for the
						Front-End and Node.js, and Express. js for the Back-End. Working on this project has
						provided me the opportunity to better understand the process of building a website.
					</div>

					<div class="mb-2 flex flex-row flex-wrap justify-center gap-2 align-middle">
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">HTML</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">CSS</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">SCSS</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">Express.js</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">PostgreSQL</div>
					</div>

					<div class="flex flex-row justify-center gap-3 align-middle">
						<a
							class="block rounded-xl bg-blue-700 px-6 py-3 font-bold text-white shadow-2xl hover:bg-blue-600"
							target="_blank"
							href="https://ebisu-website.onrender.com/">Website</a
						>

						<a
							class="block rounded-xl bg-blue-700 px-6 py-3 font-bold text-white shadow-2xl hover:bg-blue-600"
							target="_blank"
							href="https://github.com/AlexMincu/Ebisu-website">Github</a
						>
					</div>
				</div>
			</div>
		</InView>
	</div>

	<InView>
		<!-- Other projects -->
		<h3
			class="mx-auto mb-4 min-w-0 max-w-[48rem] text-center text-3xl uppercase tracking-wide opacity-40"
		>
			Other Projects
		</h3>
	</InView>

	<div class="mx-auto flex min-w-0 max-w-[48rem] flex-col gap-4">
		{#each projects as project}
			<InView>
				<ProjectsItem {project} />
			</InView>
		{/each}
	</div>
</div>
