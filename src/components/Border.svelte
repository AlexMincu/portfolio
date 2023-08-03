<script>
	export let isVisible = false;
</script>

<div class="absolute left-0 top-0 h-full w-full">
	<!-- Top-left Corner -->
	<div
		class="absolute left-0 top-0 h-[10px] w-[50%] origin-left rounded-l-md bg-gradient-to-r from-blue-300 to-blue-600 transition duration-700 ease-in-out {isVisible
			? 'scale-x-100'
			: 'scale-x-0'}"
	>
		<div
			class="absolute right-[0.5px] top-0 h-[10px] w-[10px] translate-x-[100%] border-[5px] border-b-transparent border-l-blue-600 border-r-transparent border-t-blue-600"
		/>
	</div>

	<div
		class="absolute left-0 top-0 h-[50%] w-[10px] origin-top rounded-t-md bg-gradient-to-b from-blue-300 to-blue-600 transition duration-700 ease-in-out {isVisible
			? 'scale-y-100'
			: 'scale-y-0'}"
	>
		<div
			class="absolute bottom-[0.5px] left-0 h-[10px] w-[10px] translate-y-[100%] border-[5px] border-b-transparent border-l-blue-600 border-r-transparent border-t-blue-600"
		/>
	</div>

	<!-- Bottom-right Corner -->
	<div
		class="absolute bottom-0 right-0 h-[10px] w-[50%] origin-right rounded-br-md bg-blue-600 bg-gradient-to-l from-blue-300 to-blue-600 transition duration-700 ease-in-out {isVisible
			? 'scale-x-100'
			: 'scale-x-0'}"
	>
		<div
			class="absolute bottom-0 left-[0.5px] h-[10px] w-[10px] -translate-x-[100%] border-[5px] border-b-blue-600 border-l-transparent border-r-blue-600 border-t-transparent"
		/>
	</div>

	<div
		class="absolute bottom-0 right-0 h-[50%] w-[10px] origin-bottom rounded-br-md bg-blue-600 bg-gradient-to-t from-blue-300 to-blue-600 transition duration-700 ease-in-out {isVisible
			? 'scale-y-100'
			: 'scale-y-0'}"
	>
		<div
			class="absolute right-0 top-[0.5px] h-[10px] w-[10px] -translate-y-[100%] border-[5px] border-b-blue-600 border-l-transparent border-r-blue-600 border-t-transparent"
		/>
	</div>
</div>

<style>
</style>
