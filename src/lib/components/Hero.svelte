<script lang="ts">
	import { Play } from 'lucide-svelte';
</script>

<section class="pt-36 pb-20 px-6 max-w-[1400px] mx-auto text-center">
	<h1 class="text-6xl md:text-8xl lg:text-[6.5rem] leading-[0.95] mb-8 tracking-tight font-medium">
		Investor-Grade <br /> Due Diligence in Days
	</h1>
	
	<p class="text-lg md:text-xl text-gray-400 max-w-2xl mx-auto mb-12 font-light leading-relaxed">
		AI-moderated interviews and automated synthesis <br />
		for private equity deal teams. Faster, cheaper, auditable.
	</p>

	<button class="bg-white text-black px-7 py-3.5 rounded text-sm font-medium hover:bg-gray-200 transition-colors mb-20">
		Request a Demo
	</button>

	<!-- Video Placeholder -->
	<a 
		href="https://www.linkedin.com/feed/update/urn:li:activity:7392334980800163840/" 
		target="_blank" 
		rel="noopener noreferrer"
		class="relative w-full aspect-video md:aspect-[2/1] bg-gray-900 rounded-lg overflow-hidden group cursor-pointer block"
	>
		<img 
			src="/uploaded/1765294985248-xv1keas.jpg" 
			alt="DiligenceSquared founders" 
			class="w-full h-full object-cover opacity-80 group-hover:scale-105 transition-transform duration-700"
		/>
		<div class="absolute inset-0 flex items-center justify-center">
			<div class="bg-white/10 backdrop-blur-sm border border-white/20 px-5 py-2.5 rounded-full flex items-center gap-3 text-sm font-medium hover:bg-white/20 transition-colors">
				<Play size={14} fill="currentColor" /> Watch Demo
			</div>
		</div>
	</a>
</section>
