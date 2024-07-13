<script>
	import { page } from '$app/stores';
	import { Phone } from 'lucide-svelte';
	import Navigation from './Navigation.svelte';
</script>

<Navigation />
<footer class="flex flex-col items-center justify-center gap-6 px-8 py-8 text-white bg-black sm:px-16">
	<div class="flex flex-col items-start justify-between w-full gap-6 sm:items-center sm:flex-row">
		<div class="flex flex-col pb-2 text-sm">
			<h2 class="text-base font-semibold text-neutral-200">Prince CPA Firm, PLLC</h2>
			<p>1109 Laurel Dr SE</p>
			<p>Magee, MS 39111</p>
			<div class="flex flex-col pt-2 text-sm">
				<p>
					Telephone: <a class="hover:blue-900 hover:underline" href="tel:+16018492544"
						>(601) 849-2544</a
					>
				</p>
				<p>
					Fax: <a class="hover:blue-900 hover:underline" href="tel:+16018495147">(601) 849-5147</a>
				</p>
				<p>
					Email: <a class="hover:blue-900 hover:underline" href="mailto:info@crpcpa.com"
						>info@crpcpa.com</a
					>
				</p>
			</div>
		</div>
		<div class="flex flex-col pb-8 text-base">
			<h2 class="pb-1 text-lg font-semibold text-neutral-200">Firm Information</h2>
			<p>Mississippi Firm ID F0608</p>
			<p>Charles Robert Prince, CPA License MS 1975</p>
			<p>Mary Cathryn Slocum, CPA License MS 5931</p>
		</div>
	</div>

	<div class="flex flex-row items-center justify-center w-48">
		<a class="text-xs text-gray-600 hover:underline" href="https://greatidea.dev/" target="_blank"
			>&copy; 2024 GreatIdea.dev</a
		>
	</div>
</footer>
