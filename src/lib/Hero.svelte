<script>
	import { ChevronsRight, CreditCardIcon, LockIcon } from 'lucide-svelte';
</script>

<div
	class="relative flex items-center justify-center overflow-hidden lg:justify-start hero"
>
		<div class="flex flex-col items-center justify-center w-screen h-full gap-1 md:flex-row">
			<div
				class="flex flex-col items-center justify-center w-full h-64 px-8 bg-white bg-opacity-75 md:w-1/2 md:h-96"
			>
				<h1 class="text-4xl font-medium text-center">Client Login</h1>
				<p class="text-base text-center">
					Click here to login to your secure client portal.
				</p>
				<a
					href="https://secure.netlinksolution.com/nextgen/#/"
					target="_blank"
					class="flex flex-row items-center justify-center gap-2 px-4 py-2 mt-4 text-white bg-orange-600 rounded-lg hover:bg-orange-700"
				>
					<LockIcon size={20}/> Login <ChevronsRight size={24} />
				</a>
			</div>
			<div
				class="flex flex-col items-center justify-center w-full h-64 px-8 bg-white bg-opacity-75 md:w-1/2 md:h-96"
			>
				<h1 class="text-4xl font-medium text-center">Make a Payment</h1>
				<p class="text-base text-center">
					Quickly make credit/debit card payments towards your account.
				</p>
				<a
					href="https://swipesimple.com/links/lnk_d783542f"
					target="_blank"
					class="flex flex-row items-center justify-center gap-2 px-4 py-2 mt-4 text-white bg-orange-600 rounded-lg hover:bg-orange-700"
				>
					<CreditCardIcon size={20}/> Make a Payment <ChevronsRight size={24} />
				</a>
			</div>
		</div>
	</div>

<style>
	.hero {
		background-image: url($lib/images/home-hero.jpg);
		background-size: cover;
		background-position: center;
	}
</style>
