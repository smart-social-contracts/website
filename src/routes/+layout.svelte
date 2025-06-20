<script>
	import '../app.css';
	import { onMount } from 'svelte';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Footer, FooterCopyright, FooterLinkGroup, FooterLink } from 'flowbite-svelte';

	let scrollY = 0;
	let innerHeight = 0;

	onMount(() => {
		const handleScroll = () => scrollY = window.scrollY;
		window.addEventListener('scroll', handleScroll);
		return () => window.removeEventListener('scroll', handleScroll);
	});
</script>

<svelte:window bind:scrollY bind:innerHeight />

<div class="flex min-h-screen flex-col">
	<Navbar 
		let:hidden 
		let:toggle 
		class="fixed top-0 z-50 w-full transition-all duration-300 {scrollY > 50 ? 'bg-white/95 backdrop-blur-sm shadow-lg dark:bg-gray-900/95' : 'bg-transparent'}"
	>
		<NavBrand href="/">
			<span class="self-center whitespace-nowrap text-xl font-semibold text-gray-900 dark:text-white">
				Realms GOS
			</span>
		</NavBrand>
		<NavHamburger on:click={toggle} />
		<NavUl {hidden}>
			<NavLi href="#about">About</NavLi>
			<NavLi href="#features">Features</NavLi>
			<NavLi href="#vision">Vision</NavLi>
			<NavLi href="#architecture">Architecture</NavLi>
			<NavLi href="https://github.com/smart-social-contracts/realms" target="_blank">GitHub</NavLi>
		</NavUl>
	</Navbar>

	<main class="flex-1 pt-16">
		<slot />
	</main>

	<Footer class="bg-gray-50 dark:bg-gray-800">
		<div class="mx-auto max-w-screen-xl p-4 md:flex md:items-center md:justify-between">
			<FooterCopyright href="/" by="Smart Social Contracts" />
			<FooterLinkGroup ulClass="flex flex-wrap items-center mt-3 text-sm text-gray-500 dark:text-gray-400 sm:mt-0">
				<FooterLink href="https://github.com/smart-social-contracts/realms" target="_blank">GitHub</FooterLink>
				<FooterLink href="https://github.com/smart-social-contracts/realms/blob/main/README.md" target="_blank">Documentation</FooterLink>
				<FooterLink href="#about">About</FooterLink>
			</FooterLinkGroup>
		</div>
	</Footer>
</div>
