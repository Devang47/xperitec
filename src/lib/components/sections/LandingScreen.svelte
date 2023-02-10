<script lang="ts">
	import Swiper, { Navigation, Autoplay, EffectFade } from 'swiper';
	import { onMount } from 'svelte';

	import '$lib/styles/swiper.scss';
	import '$lib/styles/swiper-navigation.scss';
	import '$lib/styles/swiper-fade.scss';

	let slideEl: HTMLElement;

	onMount(() => {
		let swiper = new Swiper(slideEl, {
			modules: [Navigation, Autoplay, EffectFade],
			effect: 'fade',

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

<div bind:this={slideEl} class="swiper">
	<div class="swiper-wrapper bg-black">
		<div class="swiper-slide h-screen max-h-[45rem] w-screen bg-black">
			<img
				class="h-full w-full object-cover opacity-50 blur"
				src="https://images.unsplash.com/photo-1597334948330-38795f25d05d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1771&q=80"
				alt=""
			/>
		</div>
		<div class="swiper-slide h-screen max-h-[45rem] w-screen bg-black">
			<img
				class="h-full w-full object-cover opacity-50 blur"
				src="https://images.unsplash.com/photo-1578575437130-527eed3abbec?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80"
				alt=""
			/>
		</div>
	</div>
	<!-- <div class="swiper-button-next">
		<svg width="16" height="24" viewBox="0 0 16 24" fill="none" xmlns="http://www.w3.org/2000/svg">
			<path d="M2 22L12 12L2 2" stroke="white" stroke-width="5" />
		</svg>
	</div>
	<div class="swiper-button-prev">
		<svg width="17" height="26" viewBox="0 0 17 26" fill="none" xmlns="http://www.w3.org/2000/svg">
			<path d="M15 2L4 13L15 24" stroke="white" stroke-width="5" />
		</svg>
	</div> -->
</div>

<header
	class="relative z-10 flex h-screen max-h-[45rem] flex-col items-center justify-center px-4 text-center text-white md:px-6"
>
	<h1 class="text-3xl font-bold md:text-4xl">Lorem ipsum dolor</h1>

	<p
		class="mx-auto mt-8 w-11/12 max-w-lg gap-6 leading-6 text-gray-200 sm:w-10/12 md:w-full md:text-lg md:leading-7"
	>
		Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas quos, impedit, repellendus
		mollitia consequatur placeat onsectetur adipisicing.
	</p>

	<button
		class="mt-16 flex items-center justify-center gap-2 rounded-md bg-gray-200 px-5 py-2 text-sm font-semibold text-black shadow duration-100 hover:bg-white hover:shadow-xl"
	>
		Contact us

		<svg width="13" height="8" viewBox="0 0 13 8" fill="none" xmlns="http://www.w3.org/2000/svg">
			<path
				d="M12.3536 4.35355C12.5488 4.15829 12.5488 3.84171 12.3536 3.64645L9.17157 0.464466C8.97631 0.269204 8.65973 0.269204 8.46447 0.464466C8.2692 0.659728 8.2692 0.976311 8.46447 1.17157L11.2929 4L8.46447 6.82843C8.2692 7.02369 8.2692 7.34027 8.46447 7.53553C8.65973 7.7308 8.97631 7.7308 9.17157 7.53553L12.3536 4.35355ZM0 4.5H12V3.5H0V4.5Z"
				fill="#282828"
			/>
		</svg>
	</button>
</header>

<style lang="postcss">
	.swiper {
		@apply absolute top-0 left-0 right-0;
	}
</style>
