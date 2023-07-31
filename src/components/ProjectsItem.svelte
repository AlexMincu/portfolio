<script>
	// @ts-nocheck

	export let project;
</script>

<div class="w-full rounded-md shadow-xl md:h-[200px]">
	<div class="h-full md:grid md:grid-cols-[35%_65%]">
		<!-- Cover -->
		<div class="relative ml-auto hidden h-full overflow-hidden md:block">
			<img class="w-full object-cover" src={project.image_url} alt="Project Cover" />

			<div class="absolute right-0 top-0 h-full w-[50px]">
				<div
					class="absolute left-0 top-0 h-0 w-0 border-x-[25px] border-t-[100px] border-x-transparent border-t-blue-700 opacity-70"
				/>
				<div
					class="absolute bottom-0 left-0 h-0 w-0 border-x-[25px] border-b-[100px] border-x-transparent border-b-blue-500 opacity-70"
				/>

				<div
					class="absolute bottom-0 right-0 h-0 w-0 border-y-[100px] border-r-[25px] border-y-transparent border-r-white"
				/>
			</div>
		</div>

		<!-- Content -->
		<div
			class="flex h-full flex-col items-center justify-center gap-2 overflow-hidden px-4 py-6 text-center"
		>
			<div class="text-lg uppercase tracking-wide">{project.title}</div>

			<div class="text-justify text-sm text-stone-600">{project.description}</div>

			<div class="flex flex-row items-center justify-center gap-6">
				<!-- Technologies -->
				<div class="flex flex-row flex-wrap justify-center gap-2 align-middle">
					{#each project.technologies as technology}
						<div class="rounded-md border border-blue-500 px-2 py-1 text-sm italic">
							{technology}
						</div>
					{/each}
				</div>

				<!-- Links -->
				<div class="flex flex-row justify-center gap-4 align-middle">
					{#each project.links as link}
						<a
							class="block rounded-xl bg-blue-800 px-6 py-2 font-bold text-white shadow-md hover:bg-stone-700"
							target="_blank"
							href={link.url}>{link.title}</a
						>
					{/each}
				</div>
			</div>
		</div>
	</div>
</div>
