<svelte:head>
	<title>Contact</title>
	<meta name="description" content="Prince CPA Firm, PLLC" />
</svelte:head>

<script lang='ts'>
	let appointment = false;

	function handleAppointmentChange(event: Event & { currentTarget: EventTarget & HTMLSelectElement; }) {
		appointment = event.currentTarget.value === 'yes';
	}
</script>

<div class="flex flex-col items-center justify-center gap-5 p-2 sm:p-8">
	<h1 class="w-full text-2xl font-bold text-center text-blue-950">Contact Us</h1>
	<hr class="w-full border border-blue-950" />
	<!-- Need the following fields:
	1. Name 
	2. Email 
	3. Phone Number 
	4. Message
	5. Dropdown to select if they are interested in an appointment
	6. If they select yes, a calendar selection for their desired date and time 
	7. Send button -->

	<!-- Also add:
	- Contact info box with same info as about page (bottom of page) -->

	<div class="flex flex-row w-full">
		<div class="flex flex-col mb-2 text-lg w-96">
			<h1 class="w-full text-xl font-bold text-center text-blue-950">General Contact Info:</h1>
			<hr class="w-full my-2 border border-blue-950" />
			<h2 class="font-semibold text-blue-950">Prince CPA Firm, PLLC</h2>
			<p>1109 Laurel Dr SE</p>
			<p>Magee, MS 39111</p>
			<div class="flex flex-col pt-3 text-base">
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
	</div>

	<form class="flex flex-col w-full gap-4 p-4 border-2 sm:p-8 sm:w-2/3 border-blue-950 rounded-2xl">
		<div class="flex flex-col gap-2">
			<label for="name" class="text-lg font-semibold text-blue-950">Name:</label>
			<input
				type="text"
				id="name"
				name="name"
				class="p-2 border rounded-md border-blue-950"
				placeholder="John Doe"
			/>
		</div>
		<div class="flex flex-col gap-2">
			<label for="email" class="text-lg font-semibold text-blue-950">Email:</label>
			<input
				type="email"
				id="email"
				name="email"
				class="p-2 border rounded-md border-blue-950"
				placeholder="email@example.com"
			/>
		</div>
		<div class="flex flex-col gap-2">
			<label for="phone" class="text-lg font-semibold text-blue-950">Phone Number:</label>
			<input
				type="tel"
				id="phone"
				name="phone"
				class="p-2 border rounded-md border-blue-950"
				placeholder="(555) 555-5555"
			/>
		</div>
		<div class="flex flex-col gap-2">
			<label for="message" class="text-lg font-semibold text-blue-950">Message:</label>
			<textarea
				id="message"
				name="message"
				class="p-2 border rounded-md border-blue-950"
				placeholder="Enter your message here..."
			/>
		</div>
		<div class="flex flex-col gap-2">
			<label for="appointment" class="text-lg font-semibold text-blue-950">Are you interested in scheduling an appointment?</label>
			<select
				id="appointment"
				name="appointment"
				class="p-2 border rounded-md border-blue-950"
				on:change={handleAppointmentChange}
			>
				<option value='yes'>Yes</option>
				<option selected value='no'>No</option>
			</select>
		</div>
		{#if appointment}
			<div class="flex flex-col gap-2">
				<label for="date" class="text-lg font-semibold text-blue-950">Desired Date and Time:</label>
				<input
					type="datetime-local"
					id="date"
					name="date"
					class="p-2 border rounded-md border-blue-950"
				/>
			</div>
		{/if}
		<button
			type="submit"
			class="p-2 text-lg font-semibold text-white rounded-md bg-blue-950 hover:bg-blue-900"
		>
			Send
		</button>
	</form>
</div>
