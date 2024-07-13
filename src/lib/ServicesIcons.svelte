<script>
	import { Briefcase, Church, Scale, User } from 'lucide-svelte';
	import CtaLink from './CTALink.svelte';
</script>

<div
	class="flex flex-col flex-wrap items-center justify-center w-full gap-8 px-8 py-16 bg-neutral-200"
>
	<div class="flex flex-col items-center justify-center w-full gap-8 lg:flex-row">
		<a
			href="/contact"
			class="flex flex-row items-center justify-start w-full gap-3 group lg:w-1/2 hover:cursor-pointer"
		>
			<div class="p-4 text-white rounded-full bg-cyan-600 group-hover:bg-orange-600">
				<Church stroke="white" size={56} />
			</div>
			<div class="flex flex-col">
				<span class="pb-1 text-2xl font-semibold">Not-for-Profit Tax Services</span>
				<p>
					We understand the challenges and intricacies of not-for-profit organizations and can help you
					navigate the complexities of not-for-profit tax law.
				</p>
				<CtaLink text="Learn More" />
			</div>
		</a>
		<a
			href="/contact"
			class="flex flex-row items-center justify-start w-full gap-3 group lg:w-1/2 hover:cursor-pointer"
		>
			<div class="p-4 text-white rounded-full bg-cyan-600 group-hover:bg-orange-600">
				<Scale stroke="white" size={56} />
			</div>
			<div class="flex flex-col">
				<span class="pb-1 text-2xl font-semibold">Governmental Consulting</span>
				<p>We offer general consulting services to State and Local government agencies.</p>
				<CtaLink text="Learn More" />
			</div>
		</a>
	</div>
	<div class="flex flex-col items-center justify-center w-full gap-8 lg:flex-row">
		<a
			href="/contact"
			class="flex flex-row items-center justify-start w-full gap-3 group lg:w-1/2 hover:cursor-pointer"
		>
			<div class="p-4 text-white rounded-full bg-cyan-600 group-hover:bg-orange-600">
				<Briefcase stroke="white" size={56} />
			</div>
			<div class="flex flex-col">
				<span class="pb-1 text-2xl font-semibold">Business Tax Services</span>
				<p>
					We take care of your business for you, so you can get back to the job of running your
					business.
				</p>
				<CtaLink text="Learn More" />
			</div>
		</a>
		<a
			href="/contact"
			class="flex flex-row items-center justify-start w-full gap-3 group lg:w-1/2 hover:cursor-pointer"
		>
			<div class="flex items-center justify-center h-full">
				<div class="p-4 text-white rounded-full bg-cyan-600 group-hover:bg-orange-600">
					<User stroke="white" size={56} />
				</div>
			</div>
			<div class="flex flex-col">
				<span class="pb-1 text-2xl font-semibold">Tax Services For Individuals</span>
				<span>You get one-on-one guidance that helps manage risk and improve performance.</span>
				<CtaLink text="Learn More" />
			</div>
		</a>
	</div>
</div>
