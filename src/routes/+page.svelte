<script>
	import ActionsIcons from '$lib/ActionsIcons.svelte';
	import Hero from '$lib/Hero.svelte';
	import ServicesIcons from '$lib/ServicesIcons.svelte';
	import ServicesSliders from '$lib/ServicesSliders.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Prince CPA Firm, PLLC" />
</svelte:head>

<section>
	<Hero />
	<ServicesIcons />
	<ServicesSliders />
	<ActionsIcons />
</section>
