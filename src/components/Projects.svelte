<script>
	// @ts-nocheck

	import ProjectsItem from './ProjectsItem.svelte';
	import InView from './InView.svelte';

	const projects = [
		{
			image_url: '/projects/rps.webp',
			title: 'Rock Paper Scissors',
			description:
				'A simple game built with HTML, CSS, and vanilla JavaScript for the Foundations Course of The Odin Project Online Resource.',
			links: [
				{
					title: 'Live Demo',
					url: 'https://alexmincu.github.io/Odin_RPS/'
				},
				{
					title: 'Github',
					url: 'https://github.com/AlexMincu/Odin_RPS'
				}
			],
			technologies: ['HTML', 'CSS', 'JavaScript']
		},

		{
			image_url: '/projects/championsfood.webp',
			title: "Champion's Food",
			description:
				"Champion's Food is a Windows application that simulates a Food Delivery service. It contains 7 different pages as well as automatically generated pages for every restaurant. Built using Java SE 15, utilizing Swing and SQL for a relational database.",
			links: [
				{
					title: 'Github',
					url: 'https://github.com/AlexMincu/FoodDeliveryApp'
				}
			],
			technologies: ['Java', 'Swing', 'MVC', 'SQL']
		},

		{
			image_url: '/projects/arcanearts.webp',
			title: 'Arcane Arts',
			description:
				'Arcane Arts is an idle/clicker game made in C++ using the SFML library. The game is made from scratch, including the game engine. I developed this game with the purpose of understanding how object‑oriented programming works and how a more complex game would be built.',
			links: [
				{
					title: 'Github',
					url: 'https://github.com/AlexMincu/ArcaneArts'
				}
			],
			technologies: ['C++', 'OOP', 'SFML']
		},

		{
			image_url: '/projects/pagoda.webp',
			title: 'AutoCAD 3D Model',
			description:
				"I've created a 3D model of a traditional Japanese Pagoda using AutoCAD, trying to preserve its intricate beauty and cultural significance.",
			links: [
				{
					title: 'View Model',
					url: 'https://grabcad.com/library/japanese-pagoda-1'
				}
			],
			technologies: ['AutoCAD']
		}
	];
</script>

<div class="mt-[20vh] md:mb-[40vh]">
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
			<div
				class="mx-auto mb-16 flex w-full flex-col overflow-hidden md:grid md:h-[600px] md:grid-cols-[45%_55%] xl:w-[1280px]"
			>
				<div
					class="mb-20 flex flex-col justify-center gap-4 px-2 text-center align-middle md:pl-0 md:pr-16"
				>
					<div class="text-2xl uppercase tracking-wide">MyFitnessLog</div>
					<div class="mb-2 text-justify text-stone-600">
						MyFitnessLog is a fitness tracking web app designed to help users monitor their training
						routines. It was developed using modern technologies and cloud services.
					</div>

					<div class="mb-2 flex flex-row flex-wrap justify-center gap-2 align-middle">
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">SvelteKit</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">TypeScript</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">SkeletonUI</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">
							TailwindCSS
						</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">PostgreSQL</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">Prisma</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">Vercel</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">Supabase</div>
					</div>

					<div class="flex flex-row justify-center gap-3 align-middle">
						<a
							class="block rounded-xl bg-gradient-to-tl from-blue-400 to-blue-700 to-50% px-6 py-3 font-bold text-white shadow-lg shadow-blue-800/40 hover:to-90%"
							target="_blank"
							href="https://myfitnesslog.vercel.app/">Live Demo</a
						>

						<a
							class="block rounded-xl bg-gradient-to-tl from-blue-400 to-blue-700 to-50% px-6 py-3 font-bold text-white shadow-lg shadow-blue-800/40 hover:to-90%"
							target="_blank"
							href="https://github.com/AlexMincu/MyFitnessLog">Github</a
						>
					</div>
				</div>

				<div class="relative hidden md:block">
					<img
						class="absolute right-[15px] top-[50%] h-[80%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/myfitnesslog/myfitnesslog_tablet_preview.webp"
						alt=""
					/>

					<img
						class="absolute left-[5%] top-[40%] h-[70%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/myfitnesslog/myfitnesslog_mobile_hero.webp"
						alt=""
					/>
					<img
						class="absolute left-0 top-[60%] h-[70%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/myfitnesslog/myfitnesslog_mobile_preview.webp"
						alt=""
					/>
				</div>
			</div>
		</InView>

		<!-- Ebisu -->
		<InView>
			<div
				class="mx-auto flex w-full flex-col overflow-hidden md:grid md:h-[600px] md:grid-cols-[55%_45%] xl:w-[1280px]"
			>
				<div class="relative hidden md:block">
					<img
						class="absolute right-0 top-[40%] h-[75%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/ebisu/ebisu_desktop_preview.webp"
						alt=""
					/>

					<img
						class="absolute left-0 top-[55%] h-[85%] -translate-y-[50%] rounded-lg shadow-2xl"
						src="/projects/ebisu/ebisu_mobile_preview.webp"
						alt=""
					/>
				</div>

				<div
					class="mb-20 flex flex-col justify-center gap-4 px-2 text-center align-middle md:pl-16 md:pr-0"
				>
					<div class="text-2xl uppercase tracking-wide">Ebisu</div>
					<div class="mb-2 text-justify text-stone-600">
						Ebisu is a responsive eCommerce website. This project was created for my University’s
						Web Development course. Working on this project has provided me the opportunity to
						better understand the process of building a website.
					</div>

					<div class="mb-2 flex flex-row flex-wrap justify-center gap-2 align-middle">
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">HTML</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">SCSS</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">JavaScript</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">Node.js</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">Express.js</div>
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">PostgreSQL</div>
					</div>

					<div class="flex flex-row justify-center gap-3 align-middle">
						<a
							class="block rounded-xl bg-gradient-to-tl from-blue-400 to-blue-700 to-50% px-6 py-3 font-bold text-white shadow-lg shadow-blue-800/40 hover:to-90%"
							target="_blank"
							href="https://ebisu-website.onrender.com/">Live Demo</a
						>

						<a
							class="block rounded-xl bg-gradient-to-tl from-blue-400 to-blue-700 to-50% px-6 py-3 font-bold text-white shadow-lg shadow-blue-800/40 hover:to-90%"
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

	<div class="mx-auto flex min-w-0 max-w-[48rem] flex-col gap-6">
		{#each projects as project}
			<InView card={true}>
				<ProjectsItem {project} />
			</InView>
		{/each}
	</div>
</div>
