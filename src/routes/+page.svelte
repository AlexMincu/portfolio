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

<section
	class="mx-auto mb-28 flex min-w-0 max-w-[48rem] flex-col justify-center gap-4 align-middle"
>
	<Header />
	<Skills />
	<Education />
	<Experience />
	<Projects />
	<Contact />
</section>
