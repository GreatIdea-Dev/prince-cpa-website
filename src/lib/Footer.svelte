<script>
	import { page } from '$app/stores';
	import { Phone } from 'lucide-svelte';
</script>

<header class="flex flex-col items-center justify-center gap-6 py-8 bg-black">
	<nav>
		<ul class="flex flex-row items-center gap-3 text-lg text-white justify-stretch">
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

	<div class="flex flex-row items-center justify-center w-48">
		<a class="text-xs text-gray-600 hover:underline" href="https://gratidea.dev/" target="_blank">&copy; 2024 GreatIdea.dev</a>
	</div>
</header>
