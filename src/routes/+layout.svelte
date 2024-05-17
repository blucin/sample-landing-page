<script>
	import '../app.css';
	import { DarkMode } from 'flowbite-svelte';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	import { SalePercentSolid } from 'flowbite-svelte-icons';
	import { HexagonIcon } from 'lucide-svelte';
	import { Banner } from 'flowbite-svelte';
</script>

<Navbar>
	<NavBrand href="/">
		<HexagonIcon class="mr-2 h-7 w-7" color="#E03702" strokeWidth="4" />
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
			>Landing Page</span
		>
	</NavBrand>
	<NavHamburger />
	<div class="flex">
		<NavUl>
			<NavLi href="/">Home</NavLi>
			<NavLi href="/">About</NavLi>
			<NavLi href="/">Navbar</NavLi>
			<NavLi href="/">Pricing</NavLi>
			<NavLi href="/">Contact</NavLi>
		</NavUl>
		<DarkMode />
	</div>
</Navbar>
<slot></slot>
<Banner id="bottom-banner" position="absolute" bannerType="bottom">
	<p class="flex items-center text-sm font-normal text-gray-500 dark:text-gray-400">
		<span class="me-3 inline-flex rounded-full bg-gray-200 p-1 dark:bg-gray-600">
			<SalePercentSolid class="h-4 w-4 text-gray-500 dark:text-gray-400" />
		</span>
		<span>
			Any announcement can go<a
				href="/"
				class="ms-0 flex items-center text-sm font-medium text-primary-600 hover:underline dark:text-primary-500 md:ms-1 md:inline-flex"
				>here</a
			>
		</span>
	</p>
</Banner>
