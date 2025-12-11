<script lang="ts">
	import { ChevronRight, FileText, Type, ArrowDown } from 'lucide-svelte';

	type Props = {
		openModal: () => void;
	};

	let { openModal }: Props = $props();
</script>

<section class="py-32 border-b border-white/5">
	<div class="max-w-[1400px] mx-auto px-6">
		<div class="text-center mb-16">
			<span class="text-sm text-gray-400 block mb-3 font-medium">Built for Deal Teams</span>
			<h2 class="text-4xl md:text-5xl font-serif mb-10">How PE Firms Use DiligenceSquared</h2>
			
			<div class="inline-flex flex-wrap justify-center gap-1 p-1 bg-surface rounded-full border border-white/10">
				<button class="px-5 py-2.5 rounded-full bg-white text-black text-sm font-medium shadow-sm">Pre-LOI Diligence</button>
				<button class="px-5 py-2.5 rounded-full text-gray-400 hover:text-white text-sm font-medium transition-colors">Market Sizing</button>
				<button class="px-5 py-2.5 rounded-full text-gray-400 hover:text-white text-sm font-medium transition-colors">Customer Insights</button>
				<button class="px-5 py-2.5 rounded-full text-gray-400 hover:text-white text-sm font-medium transition-colors">Competitive Analysis</button>
			</div>
		</div>

		<div class="grid grid-cols-1 lg:grid-cols-2 gap-0 border border-white/10 rounded-xl overflow-hidden bg-surface">
			<!-- UI Mockup Side -->
			<div class="bg-gray-200/5 p-12 lg:p-20 flex items-center justify-center border-r border-white/5 min-h-[500px]">
				<div class="w-full max-w-sm flex flex-col gap-6 relative">
					<!-- Step 1 -->
					<div class="bg-white text-black p-6 rounded-lg shadow-xl z-10 border border-gray-100">
						<div class="flex justify-between items-start mb-3">
							<div class="flex items-center gap-2 font-semibold text-sm">
								<FileText size={16} /> File upload
							</div>
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded-full text-gray-500 font-medium">User Input</span>
						</div>
						<p class="text-sm mb-4 leading-relaxed text-gray-700">Ask user to upload a patent application</p>
						<div class="flex gap-2">
							<span class="text-[10px] text-gray-400 border border-gray-200 px-2 py-1 rounded-full">Output</span>
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded-full text-gray-600">Targeting Decision</span>
						</div>
					</div>

					<!-- Arrow -->
					<div class="flex justify-center text-gray-500">
						<ArrowDown size={24} strokeWidth={1.5} />
					</div>

					<!-- Step 2 -->
					<div class="bg-white text-black p-6 rounded-lg shadow-xl z-10 border border-gray-100">
						<div class="flex justify-between items-start mb-3">
							<div class="flex items-center gap-2 font-semibold text-sm">
								<Type size={16} /> Text Input
							</div>
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded-full text-gray-500 font-medium">User Input</span>
						</div>
						<p class="text-sm mb-4 leading-relaxed text-gray-700">Would you like to craft targeted claims using information about a particular product?</p>
						<div class="flex gap-2">
							<span class="text-[10px] text-gray-400 border border-gray-200 px-2 py-1 rounded-full">Output</span>
							<span class="text-[10px] bg-gray-100 px-2 py-1 rounded-full text-gray-600">Targeting Decision</span>
						</div>
					</div>

					<!-- Branches -->
					<div class="grid grid-cols-2 gap-4 mt-2">
						<div class="bg-white text-black px-4 py-2.5 rounded-full text-xs text-center shadow font-medium border border-gray-100">Condition is true</div>
						<div class="bg-white text-black px-4 py-2.5 rounded-full text-xs text-center shadow font-medium border border-gray-100">Condition is false</div>
					</div>
				</div>
			</div>

			<!-- Content Side -->
			<div class="p-12 lg:p-20 flex flex-col justify-center">
				<h3 class="text-3xl font-serif mb-6">Pre-LOI Commercial Diligence</h3>
				<p class="text-gray-400 mb-10 leading-relaxed text-lg font-light">
					Get deep market insights before committing to expensive traditional consulting. Make confident IC presentations with auditable customer data.
				</p>
				<button onclick={openModal} class="text-sm text-gray-400 hover:text-white transition-colors inline-flex items-center gap-1 group">
					Explore Use Cases <ChevronRight size={12} class="group-hover:translate-x-0.5 transition-transform" />
				</button>
			</div>
		</div>
	</div>
</section>
