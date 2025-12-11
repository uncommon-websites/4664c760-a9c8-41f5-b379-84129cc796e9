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
	import DemoRequestModal from '$lib/components/DemoRequestModal.svelte';

	let isModalOpen = $state(false);

	function openModal() {
		isModalOpen = true;
	}

	function closeModal() {
		isModalOpen = false;
	}
</script>

<Navbar {openModal} />

<main>
	<Hero {openModal} />
	<Logos />
	<Features {openModal} />
	<Stats />
	<Testimonial />
	<Solutions {openModal} />
	<GridFeatures />
</main>

<Footer {openModal} />

<DemoRequestModal isOpen={isModalOpen} onClose={closeModal} />

