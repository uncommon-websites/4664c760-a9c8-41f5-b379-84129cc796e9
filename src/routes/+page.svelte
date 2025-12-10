<script lang="ts">
	import Navbar from '$lib/components/Navbar.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import Logos from '$lib/components/Logos.svelte';
	import Features from '$lib/components/Features.svelte';
	import Stats from '$lib/components/Stats.svelte';
	import Testimonial from '$lib/components/Testimonial.svelte';
	import Solutions from '$lib/components/Solutions.svelte';
	import GridFeatures from '$lib/components/GridFeatures.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<Navbar />

<main>
	<Hero />
	<Logos />
	<Features />
	<Stats />
	<Testimonial />
	<Solutions />
	<GridFeatures />
</main>

<Footer />

