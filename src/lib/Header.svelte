<script>
	import { page } from '$app/stores';
	import { Phone } from 'lucide-svelte';
	import logo from '$lib/images/prince-logo.png';
</script>

<div class="flex flex-row items-center justify-center w-screen py-4 text-white sm:hidden bg-blue-950">
	<a href="phone:+16018492544" class="flex flex-row items-center justify-center gap-3 text-base font-medium md:text-lg">
		<Phone size={26}/>
		<span>(601) 849-2544</span>
	</a>
</div>
<header class="flex flex-col items-center justify-center gap-6 px-4 py-6 text-blue-950 bg-neutral-200">
	<div class="flex flex-row items-center justify-center w-full gap-6 sm:justify-between">
		<a href="/" class="flex flex-row items-center justify-center w-80">
			<img src={logo} alt="Prince CPA Firm, PLLC">
		</a>
		<div class="flex-row items-center justify-center hidden w-64 sm:flex">
			<a href="phone:+16018492544" class="flex flex-row items-center justify-center gap-3 text-lg font-medium">
				<Phone size={26}/>
				<span>(601) 849-2544</span>
			</a>
		</div>
	</div>

	<nav>
		<ul class="flex flex-row items-center gap-3 text-lg font-medium justify-stretch">
			<li class=" hover:pointer hover:underline" aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li class=" hover:pointer hover:underline" aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
			<li class=" hover:pointer hover:underline" aria-current={$page.url.pathname === '/services' ? 'page' : undefined}>
				<a href="/services">Services</a>
			</li>
			<li class=" hover:pointer hover:underline" aria-current={$page.url.pathname === '/contact' ? 'page' : undefined}>
				<a href="/contact">Contact</a>
			</li>
		</ul>
	</nav>
</header>
