<script>
	export let isVisible = false;
</script>

<div class="absolute left-0 top-0 h-full w-full">
	<!-- Top-left Corner -->
	<div
		class="absolute left-0 top-0 h-[5px] w-[50%] origin-left rounded-r-md bg-blue-500 transition duration-700 ease-in-out {isVisible
			? 'scale-x-100'
			: 'scale-x-0'}"
	/>
	<div
		class="absolute left-0 top-0 h-[50%] w-[5px] origin-top rounded-b-md bg-blue-500 transition duration-700 ease-in-out {isVisible
			? 'scale-y-100'
			: 'scale-y-0'}"
	/>

	<!-- Bottom-right Corner -->
	<div
		class="absolute bottom-0 right-0 h-[5px] w-[50%] origin-right rounded-l-md bg-blue-500 transition duration-700 ease-in-out {isVisible
			? 'scale-x-100'
			: 'scale-x-0'}"
	/>
	<div
		class="absolute bottom-0 right-0 h-[50%] w-[5px] origin-bottom rounded-t-md bg-blue-500 transition duration-700 ease-in-out {isVisible
			? 'scale-y-100'
			: 'scale-y-0'}"
	/>
</div>

<style>
</style>
