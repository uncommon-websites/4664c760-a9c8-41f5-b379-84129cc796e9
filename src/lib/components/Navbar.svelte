<script lang="ts">
	import { ArrowRight } from 'lucide-svelte';

	type Props = {
		openModal: () => void;
	};

	let { openModal }: Props = $props();
</script>

<div class="fixed top-0 left-0 w-full z-50 bg-background/80 backdrop-blur-md border-b border-white/5">
	<!-- Top Banner -->
	<div class="bg-background text-[11px] text-gray-400 py-2.5 text-center border-b border-white/5 tracking-wide">
		Backed by EQT & Bain expertise. <button onclick={openModal} class="text-white hover:text-gray-300 transition-colors inline-flex items-center gap-1 group">Learn about our team <ArrowRight size={10} class="group-hover:translate-x-0.5 transition-transform" /></button>
	</div>

	<!-- Navbar -->
	<nav class="max-w-[1400px] mx-auto px-6 h-16 flex items-center justify-between">
		<!-- Logo -->
		<a href="/" class="flex items-center gap-2 text-white">
			<span class="text-xl font-medium tracking-tight">Diligenced</span>
		</a>

		<!-- Links -->
		<div class="hidden md:flex items-center gap-8 text-[13px] font-medium text-gray-300">
			<button onclick={openModal} class="hover:text-white transition-colors">Platform</button>
			<button onclick={openModal} class="hover:text-white transition-colors">Case Studies</button>
			<button onclick={openModal} class="hover:text-white transition-colors">About</button>
		</div>

		<!-- CTA -->
		<button 
			onclick={openModal}
			class="text-[13px] font-medium bg-white text-black px-4 py-2 rounded hover:bg-gray-200 transition-colors"
		>
			Request Demo
		</button>
	</nav>
</div>
