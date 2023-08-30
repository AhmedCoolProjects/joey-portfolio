<script>
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
		Dropdown,
		DropdownItem,
		DropdownDivider
	} from 'flowbite-svelte';
	import { DarkMode } from 'flowbite-svelte';
	import { page } from '$app/stores';
	$: activeUrl = $page.url.pathname;
</script>

<Navbar let:hidden let:toggle>
	<NavBrand href="/">
		<img src="/favicon.png" class="mr-3 h-6 sm:h-9" alt="Joey Logo" />
		<span class="self-center whitespace-nowrap text-2xl font-semibold dark:text-white">Joey</span>
	</NavBrand>
	<NavHamburger on:click={toggle} />
	<NavUl class="text-xl" {hidden} {activeUrl}>
		<NavLi href="/">Bio</NavLi>
		<NavLi href="/resume">Resume</NavLi>
		<NavLi id="nav-menu1" class="cursor-pointer">
			Previous Works <span class="text-xs text-gray-500 dark:text-gray-400">▼</span>
		</NavLi>

		<Dropdown triggeredBy="#nav-menu1" class="w-44 z-20">
			<DropdownItem href="/previous-works">2023</DropdownItem>
			<DropdownItem href="/previous-works">2022</DropdownItem>
			<DropdownItem href="/previous-works">2021</DropdownItem>
			<DropdownItem href="/previous-works">2020</DropdownItem>
		</Dropdown>
	</NavUl>
	<DarkMode class="text-2xl" />
</Navbar>
