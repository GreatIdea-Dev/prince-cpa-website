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
			<span class="text-2xl font-semibold"
				>Prince CPA Firm, PLLC is licensed in MS and specializes in Payroll Services.</span
			>
			<p>
				When it comes to paying employees, laws and the IRS have made the payroll function a time
				consuming nightmare for the small business owner.
			</p>
			<a href="/contact"><CtaLink text="Payroll Services" /></a>
		</div>
	</div>
	<div class="flex flex-row-reverse items-start justify-start w-full gap-6">
		<img
			alt="People looking out window"
			src={tablet}
			class="hidden rounded-lg md:flex md:w-72 lg:w-96"
		/>
		<div class="flex flex-col flex-1 gap-3">
			<span class="text-2xl font-semibold">Simplify your payroll.</span>
			<p>
				Small business owners spend an average of eight hours a month performing payroll functions.
				That's 12 full days a year that could be spent generating sales, prospecting new business
				opportunities, improving products or services, or servicing customers.
			</p>
			<a href="/contact"><CtaLink text="Payroll Services" /></a>
		</div>
	</div>
	<div class="flex flex-row items-start justify-start w-full gap-6">
		<img
			alt="People looking out window"
			src={laptop}
			class="hidden rounded-lg md:flex md:w-72 lg:w-96"
		/>
		<div class="flex flex-col flex-1 gap-3">
			<span class="text-2xl font-semibold">Please call us at (601) 849-2544.</span>
			<p>
				We offer payroll solutions that meet your business's needs and enable you to spend time
				doing what you do best, running your company.
			</p>
			<a href="tel:+16018492544"><CtaLink text="Call Today" /></a>
		</div>
	</div>
</div>
