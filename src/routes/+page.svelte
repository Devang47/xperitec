<script lang="ts">
	import FIxedCta from '$lib/components/sections/FIxedCta.svelte';
	import LandingScreen from '$lib/components/sections/LandingScreen.svelte';
	import OtherCategories from '$lib/components/sections/OtherCategories.svelte';
	import '$lib/styles/app.scss';

	const categoriesData = [
		{
			img: 'https://images.unsplash.com/photo-1532094349884-543bc11b234d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2940&q=80',
			heading: 'Lorem ipsum dolor',
			description:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus necessitatibus accusantium ab commodi amet.'
		},
		{
			img: 'https://images.unsplash.com/photo-1518152006812-edab29b069ac?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80',
			heading: 'Lorem ipsum dolor',
			description:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus necessitatibus accusantium ab commodi amet.'
		},
		{
			img: 'https://images.unsplash.com/photo-1598193957036-67845e5ead00?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1769&q=80',
			heading: 'Lorem ipsum dolor',
			description:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus necessitatibus accusantium ab commodi amet.'
		},
		{
			img: 'https://images.unsplash.com/photo-1620455800201-7f00aeef12ed?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80',
			heading: 'Lorem ipsum dolor',
			description:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus necessitatibus accusantium ab commodi amet.'
		}
	];
</script>

<LandingScreen />

<FIxedCta />

<section>
	<div class="container mx-auto w-10/12 max-w-[1100px] grid-cols-2 gap-6 py-32 md:grid">
		<div class="h-[400px] w-full overflow-hidden rounded-md md:h-[600px]">
			<img
				class="h-full w-full object-cover"
				src="https://images.unsplash.com/photo-1609143739217-01b60dad1c67?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80"
				alt=""
			/>
		</div>

		<div class="mx-auto mt-6 max-w-prose text-base lg:mt-10 lg:ml-auto lg:mr-0 lg:max-w-lg">
			<h2 class="text-sm font-semibold leading-6 text-blue-500 md:text-base">About us:</h2>
			<h3
				class="text-2xl font-bold leading-8 tracking-tight text-gray-900 sm:text-4xl md:mt-2 md:text-3xl"
			>
				Xperitec trading
			</h3>
			<p class="mt-5 text-gray-500 md:mt-8">
				Lorem ipsum dolor sit amet consectetur. Proin amet fringilla a semper risus. Sed purus
				fermentum risus accumsan sed gravida amet odio. Sapien laoreet condimentum hac aliquet et
				tristique. Ultrices pellentesque massa id aliquam eu. In a aliquet eget faucibus sodales.
			</p>

			<p class="mt-4 text-gray-500">
				Lorem ipsum dolor sit amet consectetur. Proin amet fringilla a semper risus. Sed purus
				fermentum risus accumsan sed gravida amet odio. Sapien laoreet condimentum hac aliquet et
				tristique. Ultrices pellentesque massa id aliquam eu. In a aliquet eget faucibus sodales.
			</p>

			<p class="mt-4 text-gray-500">
				Lorem ipsum dolor sit amet consectetur. Proin amet fringilla a semper risus. Sed purus
				fermentum risus accumsan sed gravida amet odio. Sapien laoreet condimentum hac aliquet et
				tristique. Ultrices pellentesque massa id aliquam eu. In a aliquet eget faucibus sodales.
			</p>
		</div>
	</div>
</section>

<section>
	<div class="container mx-auto w-10/12 max-w-[1100px] py-32">
		<h2
			class="text-center text-2xl font-bold underline underline-offset-4 lg:text-3xl lg:underline-offset-8"
		>
			Our Categories:
		</h2>

		<div
			class="mx-auto mt-16 flex w-full flex-col items-center justify-center gap-8 lg:h-screen lg:max-h-[600px] lg:flex-row lg:gap-4"
		>
			{#each categoriesData as data}
				<div class="image group bg-black">
					<img
						src={data.img}
						alt=""
						class="opacity-50 duration-200 lg:opacity-100 lg:group-hover:opacity-50"
					/>

					<div
						class="absolute top-16 left-1/2 -translate-x-1/2 text-center text-white opacity-100 duration-200 lg:opacity-0 lg:group-hover:opacity-100"
					>
						<h2 class="text-2xl font-bold">{data.heading}</h2>
						<p class="mt-6 w-80">{data.description}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<OtherCategories />

<style lang="postcss">
	.image {
		flex: 1;
		transition: 0.3s ease;
		@apply relative h-[300px] w-full overflow-hidden rounded-md lg:h-full lg:w-fit;
	}

	.image img {
		@apply h-[300px] w-full object-cover lg:h-full;
	}

	.image:hover {
		flex: 2;
	}
</style>
