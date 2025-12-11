<script lang="ts">
	import { ChevronRight } from 'lucide-svelte';

	type Props = {
		title: string;
		subtitle: string;
		description: string;
		linkText: string;
		reversed?: boolean;
		openModal: () => void;
	};

	let { title, subtitle, description, linkText, reversed = false, openModal }: Props = $props();
</script>

<div class="grid grid-cols-1 md:grid-cols-2 min-h-[600px] border-b border-white/5">
	<!-- Content Side -->
	<div class="flex flex-col justify-center px-8 md:px-20 py-24 {reversed ? 'md:order-1 border-r border-white/5' : 'md:order-2'}">
		<span class="text-sm font-medium text-white mb-2">{title}</span>
		<h2 class="text-4xl md:text-5xl font-serif mb-6 leading-[1.1]">{subtitle}</h2>
		<p class="text-gray-400 mb-10 leading-relaxed max-w-md text-lg font-light">
			{description}
		</p>
		<button onclick={openModal} class="text-sm text-gray-400 hover:text-white transition-colors inline-flex items-center gap-1 group">
			{linkText} <ChevronRight size={12} class="group-hover:translate-x-0.5 transition-transform" />
		</button>
	</div>

	<!-- Visual Side -->
	<div class="bg-surface relative overflow-hidden flex items-center justify-center p-10 {reversed ? 'md:order-2' : 'md:order-1 border-r border-white/5'}">
		<slot />
	</div>
</div>
