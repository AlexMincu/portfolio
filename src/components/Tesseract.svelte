<script>
	// @ts-nocheck

	let xValue = 0;
	let yValue = 0;

	let maxX;
	let maxY;

	function mouseMoveHandler(e) {
		xValue = e.clientX;
		yValue = e.clientY;

		maxX = window.innerWidth;
		maxY = window.innerHeight;

		console.log('xValue: ', xValue);
		console.log('yValue: ', yValue);
	}

	const moveSpeed = {
		outside: {
			front: {
				scale: '0.35'
			},
			back: {
				scale: '0.35'
			},
			top: {
				translate: '200'
			},
			bottom: {
				translate: '200'
			},
			left: {
				translate: '200'
			},
			right: {
				translate: '200'
			}
		},

		top: {
			translate: '100'
		},
		bottom: {
			translate: '100'
		},
		left: {
			translate: '100'
		},
		right: {
			translate: '100'
		},
		front: {
			scale: 0.2
		},
		back: {
			scale: 0.2
		}
	};

	/*      Translate function
        translate3d(calc(-50% + ${ xValue * moveSpeed.img1.x}px), calc(-50% + ${yValue * moveSpeed.img1.y}px), 0)

		style:perspective={`1000px`}
			style:transform={`translate3d(${Math.floor(
				(xValue / maxX) * moveSpeed.outside.x
			)}px, ${Math.floor((yValue / maxY) * moveSpeed.outside.y)}px, 0)`}
    */
</script>

<svelte:window on:mousemove={mouseMoveHandler} />

<div class="relative h-screen w-screen border border-red-500">
	<!-- Tesseract -->

	<div
		style:perspective={`1000px`}
		class="relative left-[50%] top-[50%] h-[300px] w-[300px] -translate-x-[50%] -translate-y-[50%]"
	>
		<!-- Inside Cube - Fill -->
		<img class="absolute left-0 top-0 opacity-80" src="/tesseract/fill/insideCube.png" alt="" />

		<!-- Inside Cube - Wireframe -->
		<img class="absolute left-0 top-0" src="/tesseract/wireframe/insideCube.png" alt="" />

		<!-- Back Cube -->
		<img
			style:transform={`scale3d(${1 - (yValue / maxY) * moveSpeed.back.scale}, ${
				1 - (yValue / maxY) * moveSpeed.back.scale
			}, ${1 - (yValue / maxY) * moveSpeed.back.scale})`}
			class="absolute left-0 top-0 opacity-75 transition duration-700 ease-out"
			src="/tesseract/wireframe/backCube.png"
			alt=""
		/>

		<!-- Top Cube -->
		<img
			style:transform={`translate3d(0, -${Math.floor(
				(yValue / maxY) * moveSpeed.top.translate
			)}px, 0)`}
			class="absolute left-0 top-0 opacity-75 transition duration-700 ease-out"
			src="/tesseract/wireframe/topCube.png"
			alt=""
		/>

		<!-- Bottom Cube -->
		<img
			style:transform={`translate3d(0, ${Math.floor(
				(yValue / maxY) * moveSpeed.bottom.translate
			)}px, 0)`}
			class="absolute left-0 top-0 opacity-75 transition duration-700 ease-out"
			src="/tesseract/wireframe/bottomCube.png"
			alt=""
		/>

		<!-- Left Cube -->
		<img
			style:transform={`translate3d(-${Math.floor(
				(yValue / maxY) * moveSpeed.left.translate
			)}px, 0, 0)`}
			class="absolute left-0 top-0 opacity-75 transition duration-700 ease-out"
			src="/tesseract/wireframe/leftCube.png"
			alt=""
		/>

		<!-- Right Cube -->
		<img
			style:transform={`translate3d(${Math.floor(
				(yValue / maxY) * moveSpeed.right.translate
			)}px, 0, 0)`}
			class="absolute left-0 top-0 opacity-75 transition duration-700 ease-out"
			src="/tesseract/wireframe/rightCube.png"
			alt=""
		/>

		<!-- Front Cube -->
		<img
			style:transform={`scale3d(${(yValue / maxY) * moveSpeed.front.scale + 1}, ${
				(yValue / maxY) * moveSpeed.front.scale + 1
			}, ${(yValue / maxY) * moveSpeed.front.scale + 1})`}
			class="absolute left-0 top-0 opacity-75 transition duration-700 ease-out"
			src="/tesseract/wireframe/frontCube.png"
			alt=""
		/>

		<!-- Outside - Back - Fill -->
		<img
			style:transform={`scale3d(${1 - (yValue / maxY) * moveSpeed.outside.back.scale}, ${
				1 - (yValue / maxY) * moveSpeed.outside.back.scale
			}, ${1 - (yValue / maxY) * moveSpeed.outside.back.scale})`}
			class="absolute left-0 top-0 opacity-50 transition duration-700 ease-out"
			src="/tesseract/fill/outsideCube/back.png"
			alt=""
		/>

		<!-- Outside - Back - Wireframe -->
		<img
			style:transform={`scale3d(${1 - (yValue / maxY) * moveSpeed.outside.back.scale}, ${
				1 - (yValue / maxY) * moveSpeed.outside.back.scale
			}, ${1 - (yValue / maxY) * moveSpeed.outside.back.scale})`}
			class="absolute left-0 top-0 transition duration-700 ease-out"
			src="/tesseract/wireframe/outsideCube/back.png"
			alt=""
		/>

		<!-- Outside - Top - Fill-->
		<img
			style:transform={`translate3d(0, -${Math.floor(
				(yValue / maxY) * moveSpeed.outside.top.translate
			)}px, 0)`}
			class="absolute left-0 top-0 opacity-50 transition duration-700 ease-out"
			src="/tesseract/fill/outsideCube/top.png"
			alt=""
		/>

		<!-- Outside - Top - Wireframe-->
		<img
			style:transform={`translate3d(0, -${Math.floor(
				(yValue / maxY) * moveSpeed.outside.top.translate
			)}px, 0)`}
			class="absolute left-0 top-0 transition duration-700 ease-out"
			src="/tesseract/wireframe/outsideCube/top.png"
			alt=""
		/>

		<!-- Outside - Bottom - Fill -->
		<img
			style:transform={`translate3d(0, ${Math.floor(
				(yValue / maxY) * moveSpeed.outside.bottom.translate
			)}px, 0)`}
			class="absolute left-0 top-0 opacity-50 transition duration-700 ease-out"
			src="/tesseract/fill/outsideCube/bottom.png"
			alt=""
		/>

		<!-- Outside - Bottom - Wireframe -->
		<img
			style:transform={`translate3d(0, ${Math.floor(
				(yValue / maxY) * moveSpeed.outside.bottom.translate
			)}px, 0)`}
			class="absolute left-0 top-0 transition duration-700 ease-out"
			src="/tesseract/wireframe/outsideCube/bottom.png"
			alt=""
		/>

		<!-- Outside - Left - Fill-->
		<img
			style:transform={`translate3d(-${Math.floor(
				(yValue / maxY) * moveSpeed.outside.left.translate
			)}px, 0, 0)`}
			class="absolute left-0 top-0 opacity-50 transition duration-700 ease-out"
			src="/tesseract/fill/outsideCube/left.png"
			alt=""
		/>

		<!-- Outside - Left - Wireframe -->
		<img
			style:transform={`translate3d(-${Math.floor(
				(yValue / maxY) * moveSpeed.outside.left.translate
			)}px, 0, 0)`}
			class="absolute left-0 top-0 transition duration-700 ease-out"
			src="/tesseract/wireframe/outsideCube/left.png"
			alt=""
		/>

		<!-- Outside - Right - Fill -->
		<img
			style:transform={`translate3d(${Math.floor(
				(yValue / maxY) * moveSpeed.outside.right.translate
			)}px, 0, 0)`}
			class="absolute left-0 top-0 opacity-50 transition duration-700 ease-out"
			src="/tesseract/fill/outsideCube/right.png"
			alt=""
		/>

		<!-- Outside - Right - Wireframe -->
		<img
			style:transform={`translate3d(${Math.floor(
				(yValue / maxY) * moveSpeed.outside.right.translate
			)}px, 0, 0)`}
			class="absolute left-0 top-0 transition duration-700 ease-out"
			src="/tesseract/wireframe/outsideCube/right.png"
			alt=""
		/>

		<!-- Outside - Front - Fill -->
		<img
			style:transform={`scale3d(${(yValue / maxY) * moveSpeed.outside.front.scale + 1}, ${
				(yValue / maxY) * moveSpeed.outside.front.scale + 1
			}, ${(yValue / maxY) * moveSpeed.outside.front.scale + 1})`}
			class="absolute left-0 top-0 opacity-50 transition duration-700 ease-out"
			src="/tesseract/fill/outsideCube/front.png"
			alt=""
		/>

		<!-- Outside - Front - Wireframe -->
		<img
			style:transform={`scale3d(${(yValue / maxY) * moveSpeed.outside.front.scale + 1}, ${
				(yValue / maxY) * moveSpeed.outside.front.scale + 1
			}, ${(yValue / maxY) * moveSpeed.outside.front.scale + 1})`}
			class="absolute left-0 top-0 transition duration-700 ease-out"
			src="/tesseract/wireframe/outsideCube/front.png"
			alt=""
		/>
	</div>

	<!-- <img
		style:perspective={`1000px`}
		style:transform={`rotateY(${Math.floor((xValue / maxX) * 40)}deg) rotateX(${Math.floor(
			(yValue / maxY) * 40
		)}deg)`}
		class="absolute left-[10%] top-[10%] h-[100px] w-[100px] -translate-x-[50%] -translate-y-[50%] transition duration-500 ease-out"
		src="/3d-hex.jpg"
		alt=""
	/>

	<img
		style:perspective={`1000px`}
		style:transform={`rotateY(${Math.floor((xValue / maxX) * 40)}deg) rotateX(${Math.floor(
			(yValue / maxY) * 40
		)}deg)`}
		class="absolute left-[15%] top-[15%] h-[100px] w-[100px] -translate-x-[50%] -translate-y-[50%] transition duration-500 ease-out"
		src="/3d-hex.jpg"
		alt=""
	/> -->
</div>
