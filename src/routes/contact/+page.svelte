<script lang="ts">
	let appointment = false;

	function handleAppointmentChange(
		event: Event & { currentTarget: EventTarget & HTMLSelectElement }
	) {
		appointment = event.currentTarget.value === 'Yes';
	}

	let status = "";
	const handleSubmit = async (data: { currentTarget: HTMLFormElement | undefined; }) => {
		status = 'Submitting...'
		const formData = new FormData(data.currentTarget)
		const object = Object.fromEntries(formData);
		if (appointment) {
			object.date = new Date(object.date.toString()).toDateString();
		}
		const json = JSON.stringify(object);

		const response = await fetch("https://api.web3forms.com/submit", {
			method: "POST",
			headers: {
				"Content-Type": "application/json",
				Accept: "application/json",
			},
			body: json
		});
		const result = await response.json();
		if (result.success) {
			status = "Success"
		}
	}
</script>

<svelte:head>
	<title>Contact</title>
	<meta name="description" content="Prince CPA Firm, PLLC" />
</svelte:head>

<div class="flex items-center justify-center w-full">
	<div class="flex flex-col items-center justify-center w-full max-w-5xl gap-5 p-2 sm:p-8">
		<h1 class="w-full text-2xl font-bold text-center text-blue-950">Contact Us</h1>
		<hr class="w-full border border-blue-950" />
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
		{#if status == "Submitting..."}
			<span class="text-3xl font-bold text-blue-950">{status}</span>
		{/if}
		{#if status == "Success"}
			<span class="text-3xl font-bold text-blue-950">{status}!</span>
			<p class="text-lg font-semibold text-blue-950">Message sent successfully! We will be in touch with you shortly! If you requested an appointment, we will reach out to confirm the exact date and time!</p>
		{/if}
		{#if status == ""}
			<form
			class="flex flex-col w-full gap-4 p-4 border-2 sm:p-8 sm:w-3/4 border-blue-950 rounded-2xl"
			on:submit|preventDefault={handleSubmit}
		>
			<input type="hidden" name="access_key" value="6a4bed76-efbf-4cb5-951a-8d2a61554f81">
			<div class="flex flex-col gap-2">
				<label for="name" class="text-lg font-semibold text-blue-950">Name:</label>
				<input
					type="text"
					id="name"
					name="Name"
					class="p-2 border rounded-md border-blue-950"
					placeholder="John Doe"
				/>
			</div>
			<div class="flex flex-col gap-2">
				<label for="email" class="text-lg font-semibold text-blue-950">Email:</label>
				<input
					type="email"
					id="email"
					name="Email"
					class="p-2 border rounded-md border-blue-950"
					placeholder="email@example.com"
				/>
			</div>
			<div class="flex flex-col gap-2">
				<label for="phone" class="text-lg font-semibold text-blue-950">Phone Number:</label>
				<input
					type="tel"
					id="phone"
					name="Phone"
					class="p-2 border rounded-md border-blue-950"
					placeholder="(555) 555-5555"
				/>
			</div>
			<div class="flex flex-col gap-2">
				<label for="message" class="text-lg font-semibold text-blue-950">Message:</label>
				<textarea
					id="message"
					name="Message"
					class="p-2 border rounded-md border-blue-950"
					placeholder="Enter your message here..."
				/>
			</div>
			<div class="flex flex-col gap-2">
				<label for="appointment" class="text-lg font-semibold text-blue-950"
					>Are you interested in scheduling an appointment?</label
				>
				<select
					id="appointment"
					name="Requested Appointment"
					class="p-2 border rounded-md border-blue-950"
					on:change={handleAppointmentChange}
				>
					<option value="Yes">Yes</option>
					<option selected value="No">No</option>
				</select>
			</div>
			{#if appointment}
				<div class="flex flex-col gap-2">
					<label for="date" class="text-lg font-semibold text-blue-950">Desired Appointment Date:</label>
					<input
						type="date"
						id="date"
						name="Desired Appointment Date"
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
		{/if}
	
	</div>
</div>
