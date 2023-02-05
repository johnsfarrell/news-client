<script lang="ts">
	import { Timeline, TimelineItem, Button, DarkMode } from 'flowbite-svelte';
	import { onMount } from 'svelte';

	let stories = [
		{
			title: '22 dead in Chile, as firefighters battle dozens of wildfires',
			date: '1 minute ago',
			link: 'https://www.google.com'
		},
		{
			title: '22 dead in Chile, as firefighters battle dozens of wildfires',
			date: '1 minute ago',
			link: 'https://www.google.com'
		},
		{
			title: '22 dead in Chile, as firefighters battle dozens of wildfires',
			date: '1 minute ago',
			link: 'https://www.google.com'
		},
		{
			title: '22 dead in Chile, as firefighters battle dozens of wildfires',
			date: '1 minute ago',
			link: 'https://www.google.com'
		},
		{
			title: '22 dead in Chile, as firefighters battle dozens of wildfires',
			date: '1 minute ago',
			link: 'https://www.google.com'
		}
	];

	onMount(() => {
		var socket = new WebSocket('ws://localhost:8000/ws');
		socket.addEventListener('open', () => {
			console.log('Opened');
		});
	});
</script>

<DarkMode btnClass="hidden" />
<div class="flex w-[100vw] bg-gradient-to-br from-slate-800 to-slate-900 justify-center">
	<div class="pr-[10vw] pl-3">
		<Timeline>
			<TimelineItem>
				<div
					class="font-extrabold text-transparent text-5xl md:text-7xl bg-clip-text bg-gradient-to-r from-purple-400 to-pink-600 pt-10"
				>
					Live World News
				</div>
				<div class="ml-2 text-zinc-400 font-light text-xl">Live updates from across the world.</div>
			</TimelineItem>
			{#each stories as { title, date, link }}
				<TimelineItem {title} {date}>
					<a href={link}>
						<Button color="alternative" class="my-2"
							>Learn more<svg
								class="ml-2 w-3 h-3"
								fill="currentColor"
								viewBox="0 0 20 20"
								xmlns="http://www.w3.org/2000/svg"
								><path
									fill-rule="evenodd"
									d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z"
									clip-rule="evenodd"
								/></svg
							></Button
						>
					</a>
				</TimelineItem>
			{/each}

			<div class="h-10">
				<TimelineItem date={'© 2023 John Farrell . All Rights Reserved.'} customTimeClass={'m-0'} />
			</div>
		</Timeline>
	</div>
	<!-- <div class="flex items-center">
		<canvas bind:this={el} class="w-[35vw] h-[27vw]" />
	</div> -->
</div>
