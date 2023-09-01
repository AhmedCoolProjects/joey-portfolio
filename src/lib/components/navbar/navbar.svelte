<script lang="ts">
	import MenuMobile from './menuMobile.svelte';
	import PreviousWorks from './previousWorks.svelte';

	import { page } from '$app/stores';
	$: pathname = $page.url.pathname;
</script>

<!-- svelte-ignore a11y-no-noninteractive-tabindex -->
<!-- svelte-ignore a11y-label-has-associated-control -->
<!-- svelte-ignore a11y-missing-attribute -->

<div class="navbar sticky top-0 z-10 bg-base-100">
	<div class="navbar-start">
		<a href="/" class="flex-row flex items-center justify-center normal-case text-xl"
			><img src="/favicon.png" alt="Logo" class="w-11 h-11 mr-2 object-contain" />daisyUI</a
		>
	</div>
	<ul class="menu hidden space-x-2 md:flex navbar-center menu-horizontal">
		<li>
			<a
				href="/"
				class="flex {pathname === '/' &&
					'btn-active'} flex-row items-center justify-center space-x-2"
			>
				<svg width="20" height="20" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
					<path
						fill="#000000"
						d="M21 5v2H3V5h18M3 17h9v-2H3v2m0-5h18v-2H3v2m15 2a2 2 0 1 1 0 4c-1.11 0-2-.89-2-2s.9-2 2-2m-4 8v-1c0-1.1 1.79-2 4-2s4 .9 4 2v1h-8Z"
					/>
				</svg>
				Bio</a
			>
		</li>
		<li>
			<a
				href="/resume"
				class="flex {pathname === '/resume' &&
					'btn-active'} flex-row items-center justify-center space-x-2"
			>
				<svg width="20" height="20" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
					<path
						fill="#000000"
						d="M13 9h5.5L13 3.5V9M6 2h8l6 6v12a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V4c0-1.11.89-2 2-2m8 18v-1c0-1.33-2.67-2-4-2s-4 .67-4 2v1h8m-4-8a2 2 0 0 0-2 2a2 2 0 0 0 2 2a2 2 0 0 0 2-2a2 2 0 0 0-2-2Z"
					/>
				</svg>
				Resume</a
			>
		</li>
	</ul>

	<div class="navbar-end">
		<!-- previous works -->
		<PreviousWorks />
		<!-- mobile -->
		<MenuMobile />
	</div>
</div>
