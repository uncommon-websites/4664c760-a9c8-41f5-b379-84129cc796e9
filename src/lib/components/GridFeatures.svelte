<script lang="ts">
	import { Clock, DollarSign, FileCheck, Users } from 'lucide-svelte';
</script>

<section class="py-32 border-b border-white/5">
	<div class="max-w-[1400px] mx-auto px-6">
		<div class="text-center mb-24">
			<h2 class="text-4xl md:text-5xl font-serif">Why Private Equity Firms Choose Vettd</h2>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-x-8 gap-y-16">
			<div class="flex flex-col gap-6">
				<Clock size={28} class="text-white" strokeWidth={1.5} />
				<div>
					<h3 class="text-lg font-medium mb-3">Days, Not Weeks</h3>
					<p class="text-gray-400 leading-relaxed text-sm">
						Complete comprehensive market diligence before LOI. 120+ interviews in one week vs. months with traditional consulting.
					</p>
				</div>
			</div>

			<div class="flex flex-col gap-6">
				<DollarSign size={28} class="text-white" strokeWidth={1.5} />
				<div>
					<h3 class="text-lg font-medium mb-3">Fraction of the Cost</h3>
					<p class="text-gray-400 leading-relaxed text-sm">
						80% of the insight at 5% of the cost. No more $200K+ consulting bills for early-stage diligence.
					</p>
				</div>
			</div>

			<div class="flex flex-col gap-6">
				<FileCheck size={28} class="text-white" strokeWidth={1.5} />
				<div>
					<h3 class="text-lg font-medium mb-3">Fully Auditable</h3>
					<p class="text-gray-400 leading-relaxed text-sm">
						Every finding traces back to source interviews. Review transcripts and validate insights for IC presentations.
					</p>
				</div>
			</div>

			<div class="flex flex-col gap-6">
				<Users size={28} class="text-white" strokeWidth={1.5} />
				<div>
					<h3 class="text-lg font-medium mb-3">Expert Validation</h3>
					<p class="text-gray-400 leading-relaxed text-sm">
						Findings reviewed by Blackstone and BCG alumni. Human-in-the-loop ensures institutional-grade quality.
					</p>
				</div>
			</div>
		</div>
	</div>
</section>
