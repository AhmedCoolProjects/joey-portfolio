<script lang="ts">
	import { page } from '$app/stores';
	$: pathname = $page.url.pathname;
</script>

<div class="dropdown menu dropdown-end dropdown-bottom flex md:hidden">
	<ul>
		<li>
			<a tabindex="0" class="btn btn-sm p-1 m-1">
				<svg width="20" height="20" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
					<path fill="#000000" d="M3 18v-2h18v2H3Zm0-5v-2h18v2H3Zm0-5V6h18v2H3Z" />
				</svg>
			</a>
		</li>
	</ul>
	<ul
		tabindex="0"
		class="dropdown-content dropdown-bottom z-[1] menu p-2 shadow bg-base-100 rounded-box w-40"
	>
		<li>
			<a
				href="/"
				class="flex {pathname === '/' && 'btn-active'} flex-row items-center justify-start"
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
				class="flex {pathname === '/resume' && 'btn-active'} flex-row items-center justify-start"
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
</div>
