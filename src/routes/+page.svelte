<script lang="ts">
	import Header from '../components/Header.svelte';
	import Skills from '../components/Skills.svelte';
	import Education from '../components/Education.svelte';
	import Experience from '../components/Experience.svelte';
	import Projects from '../components/Projects.svelte';
	import Contact from '../components/Contact.svelte';
</script>

<svelte:head>
	<title>alMinculescu | Portfolio</title>
	<meta name="description" content="Alex Minculescu Portfolio website" />
</svelte:head>

<section class="mb-28">
	<div class="mx-auto min-w-0 max-w-[48rem]">
		<Header />
	</div>

	<div class="mx-auto min-w-0 max-w-[48rem]">
		<Skills />
	</div>

	<div class="mx-auto min-w-0 max-w-[48rem]">
		<Education />
	</div>

	<Projects />

	<div class="mx-auto min-w-0 max-w-[48rem]">
		<Experience />
	</div>

	<div class="mx-auto min-w-0 max-w-[48rem]">
		<Contact />
	</div>
</section>
