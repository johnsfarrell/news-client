<script>
	import { DarkMode, Footer, FooterCopyright } from 'flowbite-svelte';
	import '../app.postcss';
</script>

<div class="app">
	<main>
		<slot />
	</main>
	<footer>
		<Footer>
			<FooterCopyright href="/" by="John Farrell" year={2023} />
			<DarkMode />
		</Footer>
	</footer>
</div>
