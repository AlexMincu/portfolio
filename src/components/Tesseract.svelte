<script>
	// @ts-nocheck

	let xValue = 0;
	let yValue = 0;

	let maxX;
	let maxY;

	function mouseMoveHandler(e) {
		xValue = e.clientX - window.innerWidth / 2;
		yValue = e.clientY;

		maxX = window.innerWidth / 2;
		maxY = window.innerHeight;

		if (false) {
			console.log('maxX: ', maxX);
			console.log('maxY: ', maxY);
			console.log('xValue: ', xValue);
			console.log('yValue: ', yValue);
		}
	}

	const moveSpeed = {
		outside: {
			front: {
				scale: '0.30',
				rotate: '20',
				translate: '225'
			},
			back: {
				scale: '0.30',
				rotate: '20',
				translate: '125'
			},
			top: {
				translate: '125',
				rotate: '20'
			},
			bottom: {
				translate: '125',
				rotate: '20'
			},
			left: {
				translate: '125',
				rotate: '20'
			},
			right: {
				translate: '125',
				rotate: '20'
			}
		},

		inside: {
			rotate: '15'
		},

		top: {
			translate: '75',
			rotate: '20'
		},
		bottom: {
			translate: '75',
			rotate: '20'
		},
		left: {
			translate: '75',
			rotate: '20'
		},
		right: {
			translate: '75',
			rotate: '20'
		},
		front: {
			scale: '0.2',
			rotate: '20',
			translate: '200'
		},
		back: {
			scale: '0.2',
			rotate: '20',
			translate: '100'
		}
	};
</script>

<svelte:window on:mousemove={mouseMoveHandler} />

<div style:perspective={`1000px`} class="relative h-full w-full">
	<!-- Outside - Back - Fill -->
	<img
		style:transform={`translate3d(-${Math.floor(
			(yValue / maxY) * moveSpeed.outside.back.translate
		)}px, 0, 0)  rotateY(${(xValue / maxX) * moveSpeed.outside.back.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.back.rotate) / 4
		}deg) scale3d(${1 - (yValue / maxY) * moveSpeed.outside.back.scale}, ${
			1 - (yValue / maxY) * moveSpeed.outside.back.scale
		}, ${1 - (yValue / maxY) * moveSpeed.outside.back.scale})`}
		class="absolute left-0 top-0 opacity-50 transition duration-300 ease-out"
		src="/tesseract/fill/outsideCube/back.png"
		alt=""
	/>

	<!-- Outside - Back - Wireframe -->
	<img
		style:transform={`translate3d(-${Math.floor(
			(yValue / maxY) * moveSpeed.outside.back.translate
		)}px, 0, 0)  rotateY(${(xValue / maxX) * moveSpeed.outside.back.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.back.rotate) / 4
		}deg) scale3d(${1 - (yValue / maxY) * moveSpeed.outside.back.scale}, ${
			1 - (yValue / maxY) * moveSpeed.outside.back.scale
		}, ${1 - (yValue / maxY) * moveSpeed.outside.back.scale})`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/outsideCube/back.png"
		alt=""
	/>

	<!-- Back Cube -->
	<img
		style:transform={`translate3d(-${Math.floor(
			(yValue / maxY) * moveSpeed.back.translate
		)}px, 0, 0) rotateY(${(xValue / maxX) * moveSpeed.back.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.back.rotate) / 4
		}deg) scale3d(${1 - (yValue / maxY) * moveSpeed.back.scale}, ${
			1 - (yValue / maxY) * moveSpeed.back.scale
		}, ${1 - (yValue / maxY) * moveSpeed.back.scale})`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/backCube.png"
		alt=""
	/>

	<!-- Right Cube -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.right.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.right.rotate) / 4
		}deg) translate3d(${Math.floor((yValue / maxY) * moveSpeed.right.translate)}px, 0, 0)`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/rightCube.png"
		alt=""
	/>

	<!-- Outside - Right - Fill -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.outside.right.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.right.rotate) / 4
		}deg) translate3d(${Math.floor((yValue / maxY) * moveSpeed.outside.right.translate)}px, 0, 0)`}
		class="absolute left-0 top-0 opacity-50 transition duration-300 ease-out"
		src="/tesseract/fill/outsideCube/right.png"
		alt=""
	/>

	<!-- Outside - Right - Wireframe -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.outside.right.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.right.rotate) / 4
		}deg) translate3d(${Math.floor((yValue / maxY) * moveSpeed.outside.right.translate)}px, 0, 0)`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/outsideCube/right.png"
		alt=""
	/>

	<!-- Bottom Cube -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.bottom.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.bottom.rotate) / 4
		}deg) translate3d(0, ${Math.floor((yValue / maxY) * moveSpeed.bottom.translate)}px, 0)`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/bottomCube.png"
		alt=""
	/>

	<!-- Outside - Bottom - Fill -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.outside.bottom.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.bottom.rotate) / 4
		}deg) translate3d(0, ${Math.floor((yValue / maxY) * moveSpeed.outside.bottom.translate)}px, 0)`}
		class="absolute left-0 top-0 opacity-50 transition duration-300 ease-out"
		src="/tesseract/fill/outsideCube/bottom.png"
		alt=""
	/>

	<!-- Outside - Bottom - Wireframe -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.outside.bottom.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.bottom.rotate) / 4
		}deg) translate3d(0, ${Math.floor((yValue / maxY) * moveSpeed.outside.bottom.translate)}px, 0)`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/outsideCube/bottom.png"
		alt=""
	/>

	<!-- Inside Cube - Fill -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.inside.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.inside.rotate) / 4
		}deg)`}
		class="absolute left-0 top-0 opacity-75"
		src="/tesseract/fill/insideCube.png"
		alt=""
	/>

	<!-- Inside Cube - Wireframe -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.inside.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.inside.rotate) / 4
		}deg)`}
		class="absolute left-0 top-0"
		src="/tesseract/wireframe/insideCube.png"
		alt=""
	/>

	<!-- Top Cube -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.top.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.top.rotate) / 4
		}deg) translate3d(0, -${Math.floor((yValue / maxY) * moveSpeed.top.translate)}px, 0)`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/topCube.png"
		alt=""
	/>

	<!-- Left Cube -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.left.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.left.rotate) / 4
		}deg) translate3d(-${Math.floor((yValue / maxY) * moveSpeed.left.translate)}px, 0, 0)`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/leftCube.png"
		alt=""
	/>

	<!-- Front Cube -->
	<img
		style:transform={`translate3d(${Math.floor(
			(yValue / maxY) * moveSpeed.front.translate
		)}px, 0, 0) rotateY(${(xValue / maxX) * moveSpeed.front.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.front.rotate) / 4
		}deg) scale3d(${(yValue / maxY) * moveSpeed.front.scale + 1}, ${
			(yValue / maxY) * moveSpeed.front.scale + 1
		}, ${(yValue / maxY) * moveSpeed.front.scale + 1})`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/frontCube.png"
		alt=""
	/>

	<!-- Outside - Top - Fill-->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.outside.top.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.top.rotate) / 4
		}deg) translate3d(0, -${Math.floor((yValue / maxY) * moveSpeed.outside.top.translate)}px, 0)`}
		class="absolute left-0 top-0 opacity-50 transition duration-300 ease-out"
		src="/tesseract/fill/outsideCube/top.png"
		alt=""
	/>

	<!-- Outside - Top - Wireframe-->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.outside.top.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.top.rotate) / 4
		}deg) translate3d(0, -${Math.floor((yValue / maxY) * moveSpeed.outside.top.translate)}px, 0)`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/outsideCube/top.png"
		alt=""
	/>

	<!-- Outside - Left - Fill-->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.outside.left.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.left.rotate) / 4
		}deg) translate3d(-${Math.floor((yValue / maxY) * moveSpeed.outside.left.translate)}px, 0, 0)`}
		class="absolute left-0 top-0 opacity-50 transition duration-300 ease-out"
		src="/tesseract/fill/outsideCube/left.png"
		alt=""
	/>

	<!-- Outside - Left - Wireframe -->
	<img
		style:transform={`rotateY(${(xValue / maxX) * moveSpeed.outside.left.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.left.rotate) / 4
		}deg) translate3d(-${Math.floor((yValue / maxY) * moveSpeed.outside.left.translate)}px, 0, 0)`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/outsideCube/left.png"
		alt=""
	/>

	<!-- Outside - Front - Fill -->
	<img
		style:transform={`translate3d(${Math.floor(
			(yValue / maxY) * moveSpeed.outside.front.translate
		)}px, 0, 0) rotateY(${(xValue / maxX) * moveSpeed.outside.front.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.front.rotate) / 4
		}deg) scale3d(${(yValue / maxY) * moveSpeed.outside.front.scale + 1}, ${
			(yValue / maxY) * moveSpeed.outside.front.scale + 1
		}, ${(yValue / maxY) * moveSpeed.outside.front.scale + 1})`}
		class="absolute left-0 top-0 opacity-50 transition duration-300 ease-out"
		src="/tesseract/fill/outsideCube/front.png"
		alt=""
	/>

	<!-- Outside - Front - Wireframe -->
	<img
		style:transform={`translate3d(${Math.floor(
			(yValue / maxY) * moveSpeed.outside.front.translate
		)}px, 0, 0) rotateY(${(xValue / maxX) * moveSpeed.outside.front.rotate}deg) rotateZ(${
			((xValue / maxX) * moveSpeed.outside.front.rotate) / 4
		}deg) scale3d(${(yValue / maxY) * moveSpeed.outside.front.scale + 1}, ${
			(yValue / maxY) * moveSpeed.outside.front.scale + 1
		}, ${(yValue / maxY) * moveSpeed.outside.front.scale + 1})`}
		class="absolute left-0 top-0 transition duration-300 ease-out"
		src="/tesseract/wireframe/outsideCube/front.png"
		alt=""
	/>
</div>
