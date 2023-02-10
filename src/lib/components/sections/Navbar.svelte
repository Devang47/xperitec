<script>
	import Logo from '$lib/icons/Logo.svelte';
	import Whatsapp from '$lib/icons/whatsapp.svelte';
</script>

<nav class="absolute inset-x-0 top-0 z-20 bg-white py-4 px-6 text-black">
	<div
		class="mx-auto flex max-w-[1100px] items-center justify-between gap-4 text-sm md:text-[15px]"
	>
		<div class="">
			<Logo />
		</div>

		<div class="flex items-center justify-center gap-6 md:gap-10">
			<a href="#about" class="hidden sm:block">
				<button> About us </button>
			</a>
			<a href="#products" class="hidden sm:block">
				<button> Products </button>
			</a>

			<div class="flex items-center justify-center gap-4">
				<button
					class="flex items-center justify-center gap-2 rounded-md bg-[#18A415] py-2 px-4 text-sm text-white"
				>
					<svg
						width="16"
						height="14"
						viewBox="0 0 16 14"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
					>
						<path
							d="M15.0667 14C13.1556 14 11.2927 13.6272 9.47822 12.8816C7.66311 12.1364 6.0557 11.1513 4.656 9.926C3.2557 8.70126 2.12978 7.29478 1.27822 5.70656C0.426074 4.11885 0 2.48889 0 0.816667C0 0.583333 0.0888888 0.388889 0.266667 0.233333C0.444444 0.0777777 0.666667 0 0.933334 0H4.53333C4.74074 0 4.92593 0.0583333 5.08889 0.175C5.25185 0.291667 5.34815 0.440741 5.37778 0.622222L5.95556 3.34444C5.98519 3.52593 5.98163 3.69107 5.94489 3.83989C5.90756 3.98922 5.82222 4.12222 5.68889 4.23889L3.55556 6.14444C4.17778 7.07778 4.95556 7.95278 5.88889 8.76944C6.82222 9.58611 7.85185 10.2926 8.97778 10.8889L11.0667 9.06111C11.2 8.94444 11.3742 8.85682 11.5893 8.79822C11.8039 8.74015 12.0148 8.72407 12.2222 8.75L15.2889 9.29444C15.4963 9.33333 15.6667 9.4207 15.8 9.55656C15.9333 9.69293 16 9.85185 16 10.0333V13.1833C16 13.4167 15.9111 13.6111 15.7333 13.7667C15.5556 13.9222 15.3333 14 15.0667 14Z"
							fill="white"
						/>
					</svg>
					<span> +91-123-1234-1234 </span>
				</button>

				<span class="text-gray-400"> | </span>

				<button>
					<Whatsapp fill="#18A415" />
				</button>
			</div>
		</div>
	</div>
</nav>
