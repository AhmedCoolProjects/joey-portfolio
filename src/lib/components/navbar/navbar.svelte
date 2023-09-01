<!-- svelte-ignore a11y-no-noninteractive-tabindex -->
<!-- svelte-ignore a11y-label-has-associated-control -->
<!-- svelte-ignore a11y-missing-attribute -->

<div class="navbar bg-base-100">
	<div class="navbar-start">
		<a href="/" class="flex-row flex items-center justify-center normal-case text-xl"
			><img src="/favicon.png" alt="Logo" class="w-11 h-11 mr-2 object-contain" />daisyUI</a
		>
	</div>
	<ul class="menu navbar-center menu-horizontal">
		<li>
			<a class="flex flex-row items-center justify-center space-x-2">
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
			<a class="flex flex-row items-center justify-center space-x-2">
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
		<div class="dropdown menu dropdown-end">
			<ul>
				<li>
					<a tabindex="0" class=" flex flex-row items-center justify-center space-x-2 m-1">
						<svg
							width="20"
							height="20"
							class="mr-2"
							viewBox="0 0 2048 2048"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								fill="#000"
								d="M2048 384v1280H0V384h640V256q0-27 10-50t27-40t41-28t50-10h512q27 0 50 10t40 27t28 41t10 50v128h640zm-1280 0h512V256H768v128zM128 512v185l640 319V896h512v120l640-319V512H128zm768 512v128h256v-128H896zm1024 512V839l-640 321v120H768v-120L128 839v697h1792z"
							/>
						</svg>
						Previous Works
					</a>
				</li>
				<ul
					tabindex="0"
					class="dropdown-content z-[1] menu p-2 shadow bg-base-100 rounded-box w-52"
				>
					<li><a href="/previous-works#2023">2023</a></li>
					<li><a href="/previous-works#2022">2022</a></li>
					<li><a href="/previous-works#2021">2021</a></li>
					<li><a href="/previous-works#2020">2020</a></li>
				</ul>
			</ul>
		</div>
	</div>
</div>
