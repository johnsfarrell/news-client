<script>
	import { Footer, FooterCopyright, FooterLink, FooterLinkGroup } from 'flowbite-svelte';
	import '../app.postcss';
	import Header from './Header.svelte';
	import './styles.css';
</script>

<div class="app">
	<header>
		<Header />
	</header>
	<main>
		<slot />
	</main>
	<footer>
		<Footer>
			<FooterCopyright href="/" by="John Farrell" year={2023} />
			<FooterLinkGroup
				ulClass="flex flex-wrap items-center mt-3 text-sm text-gray-500 dark:text-gray-400 sm:mt-0"
			>
				<FooterLink href="/">Home</FooterLink>
				<FooterLink href="/">About</FooterLink>
			</FooterLinkGroup>
		</Footer>
	</footer>
</div>
