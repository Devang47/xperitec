<script lang="ts">
	import Facebook from '$lib/icons/Facebook.svelte';
	import Whatsapp from '$lib/icons/whatsapp.svelte';
	import LandingScreen from './LandingScreen.svelte';
</script>

<div
	class="fixed left-6 bottom-0 z-20 hidden flex-col items-center justify-center gap-5 mix-blend-difference sm:left-10 md:left-16 md:flex md:gap-5"
	style="filter: invert(100%) brightness(1.9);"
>
	<a href="">
		<Whatsapp />
	</a>
	<a href="">
		<Facebook />
	</a>
	<div class="mt-2 h-[140px] w-px bg-[#1a0033] md:w-[2px]" />
</div>

<div
	class="fixed right-6 bottom-0 z-20 hidden flex-col items-center justify-center gap-3 text-sm text-[#1a0033] mix-blend-difference sm:right-10 md:right-16 md:flex md:gap-5 md:text-base"
	style="filter: invert(100%) brightness(1.9);"
>
	<a href="mailto:contact@xperitec.com" class="" style="writing-mode: vertical-rl"
		>contact@xperitec.com</a
	>
	<div class="mt-2 h-[140px] w-px bg-[#1a0033] md:w-[2px]" />
</div>
