<script>
	import '../app.css';
	import { DarkMode } from 'flowbite-svelte';
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
		Footer,
		FooterCopyright,
		FooterLinkGroup,
		FooterBrand,
		FooterLink,
		FooterIcon
	} from 'flowbite-svelte';
	import { FacebookSolid, GithubSolid, DiscordSolid, TwitterSolid } from 'flowbite-svelte-icons';
	import { HexagonIcon } from 'lucide-svelte';
</script>

<div class="relative px-8">
	<Navbar
		class="fixed start-0 top-0 z-20 w-full border-b-2 bg-white/30 px-2 py-2.5 backdrop-blur-md dark:bg-black/30 sm:px-4"
	>
		<NavBrand href="/">
			<HexagonIcon class="mr-2 h-7 w-7" color="#1AA249" strokeWidth="4" />
			<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
				>Landing Page</span
			>
		</NavBrand>
		<NavHamburger />
		<NavUl>
			<NavLi href="/" active={true}>Home</NavLi>
			<NavLi href="/">About</NavLi>
			<NavLi href="/">Navbar</NavLi>
			<NavLi href="/">Pricing</NavLi>
			<NavLi href="/">Contact</NavLi>
			<NavLi class="flex"><DarkMode class="px-2 py-0" /></NavLi>
		</NavUl>
	</Navbar>
	<div class="overflow-scroll pb-16">
		<slot></slot>
	</div>
</div>

<Footer footerType="sitemap" class="border-t-2 border-gray-700">
	<div class="flex">
		<div class="hidden items-center gap-1 self-start px-6 py-8 sm:flex">
			<HexagonIcon class="h-8 w-8 text-primary-600" strokeWidth="4" />
			<p class="text-xl font-semibold text-white">Landing Page</p>
		</div>
		<div class="grid flex-1 grid-cols-2 gap-8 px-6 py-8 md:grid-cols-4">
			<div>
				<h2 class="mb-6 text-sm font-semibold uppercase text-gray-400">Company</h2>
				<FooterLinkGroup ulClass="text-gray-300">
					<FooterLink liClass="mb-4" href="/">About</FooterLink>
					<FooterLink liClass="mb-4" href="/">Careers</FooterLink>
					<FooterLink liClass="mb-4" href="/">Brand Center</FooterLink>
					<FooterLink liClass="mb-4" href="/">Blog</FooterLink>
				</FooterLinkGroup>
			</div>
			<div>
				<h2 class="mb-6 text-sm font-semibold uppercase text-gray-400">Download</h2>
				<FooterLinkGroup ulClass="text-gray-300">
					<FooterLink liClass="mb-4" href="/">Discord Server</FooterLink>
					<FooterLink liClass="mb-4" href="/">Twitter</FooterLink>
					<FooterLink liClass="mb-4" href="/">Facebook</FooterLink>
					<FooterLink liClass="mb-4" href="/">Contact Us</FooterLink>
				</FooterLinkGroup>
			</div>
			<div>
				<h2 class="mb-6 text-sm font-semibold uppercase text-gray-400">Legal</h2>
				<FooterLinkGroup ulClass="text-gray-300">
					<FooterLink liClass="mb-4" href="/">Privacy Policy</FooterLink>
					<FooterLink liClass="mb-4" href="/">Licensing</FooterLink>
					<FooterLink liClass="mb-4" href="/">Terms & Conditions</FooterLink>
				</FooterLinkGroup>
			</div>
			<div>
				<h2 class="mb-6 text-sm font-semibold uppercase text-gray-400">Download</h2>
				<FooterLinkGroup ulClass="text-gray-300">
					<FooterLink liClass="mb-4" href="/">iOS</FooterLink>
					<FooterLink liClass="mb-4" href="/">Android</FooterLink>
					<FooterLink liClass="mb-4" href="/">Windows</FooterLink>
					<FooterLink liClass="mb-4" href="/">MacOS</FooterLink>
				</FooterLinkGroup>
			</div>
		</div>
	</div>
	<div class="bg-gray-700 px-4 py-6 md:flex md:items-center md:justify-between">
		<FooterCopyright
			spanClass="text-sm text-gray-300 sm:text-center"
			href="/"
			by="Landing Page™"
		/>
		<div class="mt-4 flex space-x-6 sm:justify-center md:mt-0 rtl:space-x-reverse">
			<FooterIcon href="/">
				<FacebookSolid
					class="h-5 w-5 text-gray-500 hover:text-gray-900 dark:text-gray-500 dark:hover:text-white"
				/>
			</FooterIcon>
			<FooterIcon href="/">
				<DiscordSolid
					class="h-5 w-5 text-gray-500 hover:text-gray-900 dark:text-gray-500 dark:hover:text-white"
				/>
			</FooterIcon>
			<FooterIcon href="/">
				<TwitterSolid
					class="h-5 w-5 text-gray-500 hover:text-gray-900 dark:text-gray-500 dark:hover:text-white"
				/>
			</FooterIcon>
			<FooterIcon href="/">
				<GithubSolid
					class="h-5 w-5 text-gray-500 hover:text-gray-900 dark:text-gray-500 dark:hover:text-white"
				/>
			</FooterIcon>
		</div>
	</div>
</Footer>
