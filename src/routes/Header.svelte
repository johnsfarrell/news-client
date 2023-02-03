<script>
	import { Navbar, NavBrand, Button, Input, DarkMode } from 'flowbite-svelte';
</script>

<Navbar let:hidden let:toggle>
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
			Exchangely
		</span>
	</NavBrand>
	<div class="flex md:order-2">
		<div class="relative md:block">
			<div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					class="w-6 h-6 dark:text-white"
					><path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z"
					/></svg
				>
			</div>
			<Input id="search-navbar" class="pl-10" placeholder="Search..." />
		</div>
		<DarkMode class="ml-2" />
	</div>
</Navbar>
