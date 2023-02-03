<script>
	import { Badge, Heading, P, Rating } from 'flowbite-svelte';
	import TickerTabs from './TickerTabs.svelte';
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="display-flex aligncontent-center">
	<div>
		<Heading
			tag="h1"
			class="my-12"
			customSize="flex justify-between text-4xl font-extrabold  md:text-5xl lg:text-6xl sm:px-16 xl:px-48"
			><div>
				Tesla Inc <Badge color="dark">TSLA:NASDAQ</Badge>
				<Rating class="mt-4" total={5} rating={3.21}>
					<p slot="text" class="ml-2 text-sm font-medium text-gray-500 dark:text-gray-400">
						3.21 out of 5 from 1,000+ analysts
					</p>
				</Rating>
			</div>
			<div class="flex text-xl md:text-2xl flex-col items-end p-4">
				197.35
				<div class="flex text-md md:text-lg flex-col items-end text-green-400 font-normal">
					+9.08 (+4.82%)
				</div>
			</div>
		</Heading>
	</div>
	<P class="mb-20 text-lg lg:text-xl sm:px-16 xl:px-48 dark:text-gray-400"><TickerTabs /></P>
</div>
