<script>
	// @ts-nocheck

	export let project;
</script>

<div class="w-full rounded-md border-2 border-stone-900 p-2 shadow-lg md:w-[23rem]">
	<div class="flex flex-col justify-center gap-3 text-center align-middle">
		<!-- Cover -->
		<img class="mx-auto h-64 w-full object-cover" src={project.image_url} alt="Project Cover" />

		<!-- Title -->
		<div class="text-xl">{project.title}</div>

		<!-- Technologies -->
		<div class="flex flex-row flex-wrap justify-center gap-2 align-middle">
			{#each project.technologies as technology}
				<div class="rounded-xl border border-slate-600 px-2 text-sm italic">{technology}</div>
			{/each}
		</div>

		<!-- Links -->
		<div class="flex flex-row justify-center gap-4 align-middle">
			{#each project.links as link}
				<a
					class="block rounded-xl bg-stone-800 px-4 py-2 font-bold text-white shadow-md hover:bg-stone-700"
					target="_blank"
					href={link.url}>{link.title}</a
				>
			{/each}
		</div>

		<!-- Description -->
		<div class="hidden text-justify">{project.description}</div>
	</div>
</div>
