<script>
	import { page } from '$app/stores';
</script>
    
    <nav class="flex flex-row items-center justify-center w-screen overflow-hidden bg-blue-950">
		<ul class="flex flex-row font-medium text-white items-centertext-lg justify-stretch">
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a
					class="flex items-center justify-center h-12 px-8 border-l-2 border-r border-white hover:cursor-pointer hover:bg-blue-900"
					href="/">Home</a
				>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a
					class="flex items-center justify-center h-12 px-8 border-white border-x hover:cursor-pointer hover:bg-blue-900"
					href="/about">About</a
				>
			</li>
			<li aria-current={$page.url.pathname === '/services' ? 'page' : undefined}>
				<a
					class="flex items-center justify-center h-12 px-8 border-white border-x hover:cursor-pointer hover:bg-blue-900"
					href="/services">Services</a
				>
			</li>
			<li aria-current={$page.url.pathname === '/contact' ? 'page' : undefined}>
				<a
					class="flex items-center justify-center h-12 px-8 border-l border-r-2 lg:border-r hover:cursor-pointer hover:bg-blue-900"
					href="/contact">Contact</a
				>
			</li>
            <li aria-current={$page.url.pathname === '/contact' ? 'page' : undefined}>
				<a
					class="items-center justify-center hidden h-12 px-8 border-l border-r lg:flex hover:cursor-pointer hover:bg-blue-900"
					href="https://secure.netlinksolution.com/nextgen/#/"
					target="_blank">Client Login</a
				>
			</li>
            <li aria-current={$page.url.pathname === '/contact' ? 'page' : undefined}>
				<a
					class="items-center justify-center hidden h-12 px-8 border-l border-r-2 lg:flex hover:cursor-pointer hover:bg-blue-900"
					href="https://swipesimple.com/links/lnk_d783542f"
					target="_blank">Payments</a
				>
			</li>
		</ul>
	</nav>