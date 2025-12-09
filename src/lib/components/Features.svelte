<script lang="ts">
	import FeatureSection from './FeatureSection.svelte';
	import { MessageSquare, FileSearch, Globe, BarChart3 } from 'lucide-svelte';
</script>

<section>
	<div class="py-24 text-center border-b border-white/5">
		<h2 class="text-3xl md:text-4xl font-serif">
			Complete Due Diligence Platform <br />
			Built for Speed and Precision
		</h2>
	</div>

	<!-- Feature 1: AI Interviews -->
	<FeatureSection
		title="AI-Moderated Interviews"
		subtitle="Human-Level Depth at Machine Speed"
		description="Conduct 120+ expert interviews in a week. Our AI agents ask follow-up questions, probe deeper, and capture nuanced insights that traditional surveys miss."
		linkText="See Interview Capabilities"
		reversed={false}
	>
		<!-- Interview UI Mockup -->
		<div class="bg-white text-black p-8 rounded shadow-2xl w-full max-w-md relative">
			<div class="flex items-start gap-3 mb-4">
				<div class="w-8 h-8 rounded-full bg-gray-200 flex items-center justify-center flex-shrink-0">
					<MessageSquare size={16} />
				</div>
				<div class="flex-1">
					<p class="text-sm text-gray-600 mb-1">AI Interviewer</p>
					<p class="text-sm leading-relaxed">
						"Can you walk me through your decision-making process when evaluating vendors in this space? What factors matter most?"
					</p>
				</div>
			</div>
			<div class="flex items-start gap-3 mb-4">
				<div class="w-8 h-8 rounded-full bg-gray-800 flex items-center justify-center flex-shrink-0 text-white text-xs">
					EX
				</div>
				<div class="flex-1">
					<p class="text-sm text-gray-600 mb-1">Expert Response</p>
					<p class="text-sm leading-relaxed">
						"Price is important, but reliability and integration capabilities are actually the primary drivers..."
					</p>
				</div>
			</div>
			<div class="absolute bottom-4 right-4 w-3 h-3 bg-green-500 rounded-full animate-pulse"></div>
		</div>
	</FeatureSection>

	<!-- Feature 2: Automated Synthesis -->
	<FeatureSection
		title="Automated Synthesis"
		subtitle="From Raw Data to Investment Insights"
		description="Our AI analyzes hundreds of interviews and synthesizes findings into clear, actionable reports. Every insight is traceable to its source for complete auditability."
		linkText="View Sample Reports"
		reversed={true}
	>
		<!-- Synthesis UI Mockup -->
		<div class="bg-white text-black p-6 rounded shadow-2xl w-full max-w-md text-xs">
			<div class="mb-4 pb-3 border-b border-gray-200">
				<h3 class="font-semibold text-sm mb-2">Market Size & Growth</h3>
				<p class="text-gray-600 text-xs leading-relaxed mb-2">
					TAM estimated at $2.3B growing 18% annually <sup class="bg-gray-200 px-1 rounded">12</sup> <sup class="bg-gray-200 px-1 rounded">18</sup>
				</p>
			</div>
			<div class="mb-4 pb-3 border-b border-gray-200">
				<h3 class="font-semibold text-sm mb-2">Competitive Position</h3>
				<p class="text-gray-600 text-xs leading-relaxed mb-2">
					Target leads in enterprise segment with 34% share <sup class="bg-gray-200 px-1 rounded">7</sup> <sup class="bg-gray-200 px-1 rounded">23</sup>
				</p>
			</div>
			<div>
				<h3 class="font-semibold text-sm mb-2">Key Risks</h3>
				<p class="text-gray-600 text-xs leading-relaxed">
					Customer concentration: top 3 = 42% revenue <sup class="bg-gray-200 px-1 rounded">31</sup>
				</p>
			</div>
		</div>
	</FeatureSection>

	<!-- Feature 3: Multilingual -->
	<FeatureSection
		title="Global Reach"
		subtitle="Multilingual Capabilities"
		description="Conduct interviews in local languages across 5+ countries simultaneously. Our AI voice agents handle Nordic, European, and Asian markets with native fluency."
		linkText="See Language Support"
		reversed={false}
	>
		<!-- Multilingual UI Mockup -->
		<div class="grid grid-cols-2 gap-4 w-full max-w-md">
			<div class="bg-white text-black p-6 rounded shadow-lg flex flex-col items-center text-center gap-4 aspect-square justify-center hover:scale-[1.02] transition-transform duration-300">
				<Globe size={32} strokeWidth={1.5} />
				<span class="font-medium text-sm">English</span>
			</div>
			<div class="bg-white text-black p-6 rounded shadow-lg flex flex-col items-center text-center gap-4 aspect-square justify-center hover:scale-[1.02] transition-transform duration-300">
				<Globe size={32} strokeWidth={1.5} />
				<span class="font-medium text-sm">Danish</span>
			</div>
			<div class="bg-white text-black p-6 rounded shadow-lg flex flex-col items-center text-center gap-4 aspect-square justify-center hover:scale-[1.02] transition-transform duration-300">
				<Globe size={32} strokeWidth={1.5} />
				<span class="font-medium text-sm">German</span>
			</div>
			<div class="bg-white text-black p-6 rounded shadow-lg flex flex-col items-center text-center gap-4 aspect-square justify-center hover:scale-[1.02] transition-transform duration-300">
				<Globe size={32} strokeWidth={1.5} />
				<span class="font-medium text-sm">Swedish</span>
			</div>
		</div>
	</FeatureSection>

	<!-- Feature 4: Interactive Reports -->
	<FeatureSection
		title="Interactive Reports"
		subtitle="Full Auditability & Traceability"
		description="Every finding links back to source interviews. Review transcripts, validate insights, and drill down into the data. Built for the scrutiny of Investment Committees."
		linkText="Explore Platform"
		reversed={true}
	>
		<!-- Reports UI Mockup -->
		<div class="bg-white text-black p-6 rounded shadow-2xl w-full max-w-md text-xs">
			<div class="flex items-center justify-between mb-4 pb-3 border-b border-gray-200">
				<div class="flex items-center gap-2">
					<FileSearch size={16} />
					<span class="font-semibold text-sm">Finding Details</span>
				</div>
				<span class="text-[10px] bg-gray-100 px-2 py-1 rounded-full">Validated</span>
			</div>
			<p class="text-gray-700 text-xs mb-3 leading-relaxed">
				"Customers cite integration complexity as primary barrier to adoption"
			</p>
			<div class="space-y-2">
				<div class="flex items-center justify-between text-[10px] text-gray-500 hover:bg-gray-50 p-2 rounded cursor-pointer">
					<span>Interview #12 - VP Engineering, Enterprise Co.</span>
					<span class="text-gray-400">→</span>
				</div>
				<div class="flex items-center justify-between text-[10px] text-gray-500 hover:bg-gray-50 p-2 rounded cursor-pointer">
					<span>Interview #27 - CTO, Mid-Market SaaS</span>
					<span class="text-gray-400">→</span>
				</div>
				<div class="flex items-center justify-between text-[10px] text-gray-500 hover:bg-gray-50 p-2 rounded cursor-pointer">
					<span>Interview #45 - Dir. IT, Fortune 500</span>
					<span class="text-gray-400">→</span>
				</div>
			</div>
		</div>
	</FeatureSection>
</section>
