<script>
	import people from '$lib/images/people-looking-out-window.jpg';
	import tablet from '$lib/images/typing-on-tablet.jpg';
	import laptop from '$lib/images/success-laptop.jpg';
	import CtaLink from './CTALink.svelte';
</script>

<div class="flex flex-col items-center justify-center w-full gap-16 px-8 py-16">
	<div class="flex flex-row items-start justify-start w-full gap-6">
		<img
			alt="People looking out window"
			src={people}
			class="hidden rounded-lg md:flex md:w-72 lg:w-96"
		/>
		<div class="flex flex-col flex-1 gap-3">
			<span class="text-2xl font-semibold">Governmental Consulting</span>
			<p>
				We know accuracy and efficiency is of the upmost importance concerning Governmental
				Consulting. Whether the consultation is for federal, state, or a local governing office, we
				have you covered.
			</p>
			<a href="/contact"><CtaLink text="Schedule a consultation today!" /></a>
		</div>
	</div>
	<div class="flex flex-row-reverse items-start justify-start w-full gap-6">
		<img
			alt="People looking out window"
			src={tablet}
			class="hidden rounded-lg md:flex md:w-72 lg:w-96"
		/>
		<div class="flex flex-col flex-1 gap-3">
			<span class="text-2xl font-semibold">Nonprofit Accounting</span>
			<p>
				Let us take the guess work out of Nonprofit Accounting. This unique situation requires a
				specific attention to detail and organization, which will be received from Prince CPA.
			</p>
			<a href="/contact"><CtaLink text="Learn more" /></a>
		</div>
	</div>
	<div class="flex flex-row items-start justify-start w-full gap-6">
		<img
			alt="People looking out window"
			src={laptop}
			class="hidden rounded-lg md:flex md:w-72 lg:w-96"
		/>
		<div class="flex flex-col flex-1 gap-3">
			<span class="text-2xl font-semibold">Tax Services for Businesses and Individuals</span>
			<p>
				We offer tax services for businesses and individuals alike. At Prince CPA, rest assured we
				will go above and beyond to ensure your unique needs are met.
			</p>
			<a href="tel:+16018492544"><CtaLink text="Call Today" /></a>
		</div>
	</div>
</div>
