<script lang="ts">
	import "../app.css";
	let { children } = $props();

	import { Navbar, NavBrand, NavHamburger, NavUl, NavLi } from 'flowbite-svelte';

</script>
<div class="h-screen flex flex-col">
	<Navbar>
		<NavBrand href="/">
			<span
				class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
				>CountryName</span
			>
		</NavBrand>
		<NavHamburger />
		<NavUl>
			<NavLi href="/">Home</NavLi>
			<NavLi href="/search">Search</NavLi>
			<NavLi href="/info">Info</NavLi>
		</NavUl>
	</Navbar>
	<div class="flex-grow">
		{@render children()}
	</div>
</div>
