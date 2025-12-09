<script lang="ts">
	import { ChevronRight } from 'lucide-svelte';
</script>

<section class="py-12 border-b border-white/5">
	<div class="max-w-[1400px] mx-auto px-6">
		<div class="text-center mb-10">
			<p class="text-xl font-serif text-gray-200">Trusted by Leading Private Equity Firms</p>
		</div>

		<!-- Logos Grid -->
		<div class="flex flex-wrap justify-center items-center gap-x-16 gap-y-10 opacity-60 grayscale hover:grayscale-0 transition-all duration-500">
			<span class="text-xl font-sans font-black tracking-tighter text-white">AXCEL</span>
			<span class="text-lg font-serif font-bold tracking-widest text-white">BLACKSTONE</span>
			<span class="text-xl font-sans font-black tracking-tighter text-white">KKR</span>
			<span class="text-lg font-sans font-bold tracking-wide text-white">CARLYLE</span>
			<span class="text-xl font-serif font-bold tracking-widest text-white">APOLLO</span>
			<span class="text-lg font-sans font-bold text-white">TPG</span>
			<span class="text-xl font-serif text-white">Warburg Pincus</span>
		</div>

		<div class="text-center mt-12">
			<a href="#" class="text-sm text-gray-400 hover:text-white transition-colors inline-flex items-center gap-1">
				See Case Studies <ChevronRight size={12} />
			</a>
		</div>
	</div>
</section>
