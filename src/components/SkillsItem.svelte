<script>
	export let imgUrl = '';
	export let title = '';
</script>

<div
	class="relative h-full w-full opacity-[0.85] transition duration-300 ease-out md:opacity-60 md:hover:opacity-100"
>
	<div class="absolute h-full w-full opacity-0" />

	<div class="flex flex-col items-center justify-start">
		<div class="w-[80%]">
			<img class="" src={imgUrl} alt="" />
		</div>
		<div class=" text-center font-semibold tracking-wide">{title}</div>
	</div>
</div>
