<script>
	import { ChevronsRight } from 'lucide-svelte';
</script>

<div
	class="relative flex items-center justify-center px-1 overflow-hidden lg:justify-start py-36 lg:px-36 hero"
>
	<div
		class="flex flex-col items-center justify-center px-16 py-8 bg-white bg-opacity-75 lg:px-20 rounded-xl"
	>
		<h1 class="text-xl font-medium">Our business counts on</h1>
		<p class="text-5xl font-medium">Your Success</p>
		<a
			href="/contact"
			class="flex flex-row items-center justify-center gap-1 px-4 py-2 mt-4 text-white bg-orange-600 rounded-lg hover:bg-orange-700"
		>
			Schedule A Consultation <ChevronsRight size={24} />
		</a>
	</div>
</div>

<style>
	.hero {
		background-image: url($lib/images/home-hero.jpg);
		background-size: cover;
		background-position: center;
	}
</style>
