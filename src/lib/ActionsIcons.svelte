<script>
	import { Calendar, CreditCard, MessageCircleQuestion, UserRoundIcon } from 'lucide-svelte';
	import CtaLink from './CTALink.svelte';
</script>

<div
	class="flex flex-col flex-wrap items-center justify-center w-full gap-8 px-8 py-16 bg-neutral-200"
>
	<div class="flex flex-col items-center justify-center w-full gap-8 lg:flex-row">
		<a
			href="https://secure.netlinksolution.com/nextgen/#/"
			class="flex flex-row items-center justify-start w-full gap-3 group lg:w-1/2 hover:cursor-pointer"
		>
			<div class="p-4 text-white rounded-full bg-cyan-600 group-hover:bg-orange-600">
				<UserRoundIcon stroke="white" size={56} />
			</div>
			<div class="flex flex-col">
				<span class="pb-1 text-2xl font-semibold">Client Portal</span>
				<p>Click here to login to your secure client portal.</p>
				<CtaLink text="Client Login" />
			</div>
		</a>
		<a
			href="https://swipesimple.com/links/lnk_d783542f"
			class="flex flex-row items-center justify-start w-full gap-3 group lg:w-1/2 hover:cursor-pointer"
		>
			<div class="p-4 text-white rounded-full bg-cyan-600 group-hover:bg-orange-600">
				<CreditCard stroke="white" size={56} />
			</div>
			<div class="flex flex-col">
				<span class="pb-1 text-2xl font-semibold">Make a Payment</span>
				<p>Quickly make credit/debit card payments towards your account.</p>
				<CtaLink text="Make a Payment" />
			</div>
		</a>
	</div>
	<div class="flex flex-col items-center justify-center w-full gap-8 lg:flex-row">
		<a
			href="/contact"
			class="flex flex-row items-center justify-start w-full gap-3 group lg:w-1/2 hover:cursor-pointer"
		>
			<div class="p-4 text-white rounded-full bg-cyan-600 group-hover:bg-orange-600">
				<Calendar stroke="white" size={56} />
			</div>
			<div class="flex flex-col">
				<span class="pb-1 text-2xl font-semibold">We Are Here to Help</span>
				<p>We will happily offer you a free consultation to determine how we can best serve you.</p>
				<CtaLink text="Contact Us" />
			</div>
		</a>
		<a
			href="/contact"
			class="flex flex-row items-center justify-start w-full gap-3 group lg:w-1/2 hover:cursor-pointer"
		>
			<div class="flex items-center justify-center h-full">
				<div class="p-4 text-white rounded-full bg-cyan-600 group-hover:bg-orange-600">
					<MessageCircleQuestion stroke="white" size={56} />
				</div>
			</div>
			<div class="flex flex-col">
				<span class="pb-1 text-2xl font-semibold">Ask a Question</span>
				<span
					>Find comfort in knowing an expert in accounting is only an email or phone-call away.</span
				>
				<CtaLink text="(601) 849-2544" />
			</div>
		</a>
	</div>
</div>
