<script>
	import InView from './InView.svelte';
	import Border from './Border.svelte';
	import SkillsItem from './SkillsItem.svelte';
</script>

<InView let:isVisible>
	<div class="relative mt-[15vh] py-[10vh] md:mb-[50vh] md:px-[5vh]">
		<Border {isVisible} />

		<h2 class="mb-4 text-center text-5xl uppercase tracking-widest opacity-40">Skills & Tools</h2>

		<div class="mx-8 grid grid-cols-3 gap-x-4 gap-y-2 md:mx-5 md:grid-cols-6 md:gap-x-0">
			<SkillsItem imgUrl="/skills/cpp.png" title="C/C++" />

			<SkillsItem imgUrl="/skills/java.png" title="Java" />

			<SkillsItem imgUrl="/skills/python.png" title="Python" />

			<SkillsItem imgUrl="/skills/javascript.png" title="JavaScript" />

			<SkillsItem imgUrl="/skills/typescript.png" title="TypeScript" />

			<SkillsItem imgUrl="/skills/html.png" title="HTML" />

			<SkillsItem imgUrl="/skills/css.png" title="CSS" />

			<SkillsItem imgUrl="/skills/tailwind.png" title="TailWindCSS" />

			<SkillsItem imgUrl="/skills/svelte.png" title="SvelteKit" />

			<SkillsItem imgUrl="/skills/postgres.png" title="PostgreSQL" />

			<SkillsItem imgUrl="/skills/prisma.png" title="Prisma" />

			<SkillsItem imgUrl="/skills/sequelize.png" title="Sequelize" />

			<SkillsItem imgUrl="/skills/git.png" title="Git" />

			<SkillsItem imgUrl="/skills/bash.png" title="Bash" />

			<SkillsItem imgUrl="/skills/photoshop.png" title="Adobe Photoshop" />

			<SkillsItem imgUrl="/skills/figma.png" title="Figma" />
		</div>
	</div>
</InView>
