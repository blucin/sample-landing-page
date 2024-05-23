<script>
	import { Heading, P, Button, Marquee, Card, Badge } from 'flowbite-svelte';
	import { ArrowRightOutline } from 'flowbite-svelte-icons';
	import CustomCard from '../components/card.svelte';
</script>

<div class="mt-16 py-8 lg:p-8">
	<section class="block lg:flex lg:items-center lg:px-40 lg:py-16">
		<div class="space-y-5">
			<div>
				<Heading>Lessons and insights</Heading>
				<Heading class="text-primary-600 dark:text-primary-700">from 8 years</Heading>
				<P class="mt-3 text-pretty text-gray-500 dark:text-gray-400">
					Where to grow your business as a photographer: site or social media?
				</P>
			</div>
			<Button class="w-[150px] bg-primary-600 font-semibold shadow-lg shadow-green-500/50" size="md"
				>Register</Button
			>
		</div>
		<img
			src="images/Illustration.svg"
			alt="Illustration"
			class="w-200 h-200 ml-auto hidden dark:brightness-75 lg:block"
		/>
	</section>

	<section class="mt-16 flex flex-col items-center gap-2">
		<p class="text-3xl font-semibold text-gray-700 dark:text-gray-300">Our Clients</p>
		<P class="text-pretty text-sm text-gray-500 dark:text-gray-400">
			We have been working with some Fortune 500+ clients
		</P>
		<Marquee speed={0.5} class="py-5">
			<img src="/images/logos/logo-1.svg" alt="Logo 1" class="h-12 w-12 dark:invert" />
			<img src="/images/logos/logo-2.svg" alt="Logo 2" class="h-12 w-12 dark:invert" />
			<img src="/images/logos/logo-3.svg" alt="Logo 3" class="h-12 w-12 dark:invert" />
			<img src="/images/logos/logo-4.svg" alt="Logo 4" class="h-12 w-12 dark:invert" />
			<img src="/images/logos/logo-5.svg" alt="Logo 5" class="h-12 w-12 dark:invert" />
			<img src="/images/logos/logo-6.svg" alt="Logo 6" class="h-12 w-12 dark:invert" />
			<img src="/images/logos/logo-3.svg" alt="Logo 3" class="h-12 w-12 dark:invert" />
		</Marquee>
	</section>

	<section class="mt-24 flex flex-col items-center gap-2">
		<p class="text-center text-3xl font-semibold text-gray-700 dark:text-gray-300">
			Manage your entire community <br /> in a single system
		</p>
		<P class="text-pretty text-sm text-gray-500 dark:text-gray-400">Who are we suitable for?</P>
		<div class="mt-5 flex flex-col gap-10 sm:flex-row">
			{#each [{ imgUrl: 'images/system-section/public-icon.svg', title: 'Membership Organisations', description: 'Our membership management software provides full automation of membership renewals and payments' }, { imgUrl: 'images/system-section/institute-icon.svg', title: 'National Associations', description: 'Our membership management software provides full automation of membership renewals and payments' }, { imgUrl: 'images/system-section/club-icon.svg', title: 'Clubs and Groups', description: 'Our membership management software provides full automation of membership renewals and payments' }] as c, i}
				<CustomCard imageUrl={c.imgUrl} cardTitle={c.title} cardDescription={c.description} />
			{/each}
		</div>
	</section>

	<section class="mt-16 flex items-center gap-10 xl:px-60">
		<img
			src="/images/password.svg"
			width="350"
			alt="Password"
			class="hidden dark:brightness-75 lg:block"
		/>
		<div class="">
			<Heading class="text-3xl font-semibold text-gray-700 dark:text-gray-300"
				>The unseen of spending three years at Pixelgrade</Heading
			>
			<P class="mt-3 text-pretty text-gray-500 dark:text-gray-400">
				Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid, placeat facilis? Omnis,
				corporis temporibus nulla officiis autem repellat sit, harum consequuntur eum perferendis
				expedita, fugiat pariatur ab quo vel facere.
			</P>
		</div>
	</section>

	<section class="mt-16">
		<Card class="text-center mx-auto" size="lg" padding="xl">
			<h5
				class="mb-2 flex items-center justify-center text-3xl font-bold text-gray-900 dark:text-white"
			>
				Try our premium service <Badge class="ms-2 font-semibold">PRO</Badge>
			</h5>
			<P class="mb-5 text-pretty text-gray-500 dark:text-gray-400">
				Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid, placeat facilis? Omnis,
				corporis temporibus nulla officiis autem repellat sit, harum consequuntur eum perferendis
				expedita, fugiat pariatur ab quo vel facere.
			</P>
			<div
				class="items-center justify-center space-y-4 sm:flex sm:space-x-4 sm:space-y-0 rtl:space-x-reverse"
			>
				<Button class="font-bold shadow-lg shadow-green-500/50">
					Get a Demo
					<ArrowRightOutline class="ms-1 h-6 w-6 text-white" />
				</Button>
			</div>
		</Card>
	</section>
</div>
