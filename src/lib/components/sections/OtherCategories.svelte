<script lang="ts">
	import Swiper, { Navigation, Autoplay } from 'swiper';
	import { onMount } from 'svelte';

	let slideEl: HTMLElement;
	onMount(() => {
		let swiper = new Swiper(slideEl, {
			slidesPerView: innerWidth > 1024 ? 4 : innerWidth > 768 ? 3 : 1,
			spaceBetween: 30,
			modules: [Navigation, Autoplay],

			autoplay: {
				delay: 3000,
				disableOnInteraction: false
			},

			navigation: {
				nextEl: '.swiper-button-next',
				prevEl: '.swiper-button-prev'
			}
		});
	});
</script>

<section>
	<div class="container relative mx-auto w-10/12 max-w-[1100px] py-10">
		<div class="swiper mySwiper" bind:this={slideEl}>
			<div class="swiper-wrapper">
				{#each new Array(10) as _}
					<div class="swiper-slide slide-image bg-black">
						<img
							class="opacity-70"
							src="https://images.unsplash.com/photo-1516387938699-a93567ec168e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1771&q=80"
							alt=""
						/>

						<div
							class="absolute top-20 left-1/2 -translate-x-1/2 text-center text-white opacity-100 duration-200"
						>
							<h2 class="text-lg font-bold">Lorem ipsum</h2>
						</div>
					</div>
				{/each}
			</div>
		</div>
		<div class="swiper-button-prev cursor-pointer">
			<svg width="14" viewBox="0 0 17 26" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path d="M15 2L4 13L15 24" stroke="black" stroke-width="5" />
			</svg>
		</div>
		<div class="swiper-button-next cursor-pointer">
			<svg width="14" viewBox="0 0 16 24" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path d="M2 22L12 12L2 2" stroke="black" stroke-width="5" />
			</svg>
		</div>
	</div>
</section>

<style lang="postcss">
	.slide-image {
		@apply h-[200px] w-[200px] overflow-hidden rounded-md;
	}

	.slide-image img {
		display: block;
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	.swiper-button-prev {
		left: -30px;
		right: auto;
	}
	.swiper-button-next {
		right: -30px;
		left: auto;
	}

	@media (min-width: 768px) {
		.swiper-button-prev {
			left: -50px;
			right: auto;
		}
		.swiper-button-next {
			right: -50px;
			left: auto;
		}
	}
</style>
