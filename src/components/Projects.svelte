<script>
	// @ts-nocheck

	import ProjectsItem from './ProjectsItem.svelte';

	const projects = [
		{
			image_url: '/projects/myfitnesslog.png',
			title: 'MyFitnessLog',
			description:
				'MyFitnessLog is a fitness tracking web app designed to help users monitor their training routines. It was developed using modern technologies and cloud services - Supabase, Vercel',
			links: [
				{
					title: 'Website',
					url: 'https://myfitnesslog.vercel.app/'
				},
				{
					title: 'Github',
					url: 'https://github.com/AlexMincu/MyFitnessLog'
				}
			],
			technologies: ['SvelteKit', 'TailwindCSS', 'Typescript', 'PostgreSQL', 'Prisma']
		},

		{
			image_url: '/projects/ebisu.jpeg',
			title: 'Ebisu',
			description:
				'A fictional responsive eCommerce website. Used HTML, SCSS, and modern JavaScript for the Front-End and Node.js, and Express. js for the Back-End. Working on this project has provided me the opportunity to better understand the process of building a website.',
			links: [
				{
					title: 'Website',
					url: 'https://ebisu-website.onrender.com/'
				},
				{
					title: 'Github',
					url: 'https://github.com/AlexMincu/Ebisu-website'
				}
			],
			technologies: ['HTML', 'CSS', 'SCSS', 'Javascript', 'Node.js', 'Express.js', 'SQL']
		},

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

<div>
	<h2 class="mb-4 text-2xl">Projects</h2>

	<div class="align-start flex flex-row flex-wrap justify-center gap-4">
		{#each projects as project}
			<ProjectsItem {project} />
		{/each}
	</div>
</div>
