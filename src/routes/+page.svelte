<script>
	import { Card, Button, Rating, Badge } from 'flowbite-svelte';
</script>

<div class="p-8">
	<Card padding="none">
		<div class="p-5">
			<div class="flex justify-between items-center">
				<a href="/">
					<h5 class="text-xl font-semibold tracking-tight text-gray-900 dark:text-white">
						Tesla Inc <Badge color="dark">TSLA:NASDAQ</Badge>
					</h5>
				</a>
				<div class="flex text-xl md:text-2xl flex-col items-end p-4 dark:text-white">
					197.35
					<div class="flex text-md md:text-lg flex-col items-end text-green-400 font-normal">
						+9.08 (+4.82%)
					</div>
				</div>
			</div>
			<div class="flex justify-between items-center">
				<Rating rating={4} size="18" class="mt-2.5 mb-5">
					<Badge slot="text" class="ml-3">1,000+</Badge>
				</Rating>
				<Button href="/">Details</Button>
			</div>
		</div>
	</Card>
</div>
