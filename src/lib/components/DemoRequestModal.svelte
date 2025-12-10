<script lang="ts">
	import { X } from 'lucide-svelte';

	type Props = {
		isOpen: boolean;
		onClose: () => void;
	};

	let { isOpen, onClose }: Props = $props();

	let formData = $state({
		firstName: '',
		lastName: '',
		email: '',
		phone: '',
		firm: '',
		title: '',
		message: ''
	});

	function handleSubmit(e: Event) {
		e.preventDefault();
		// Form submission logic will go here
		console.log('Form submitted:', formData);
		onClose();
	}

	function handleBackdropClick(e: MouseEvent) {
		if (e.target === e.currentTarget) {
			onClose();
		}
	}
</script>

{#if isOpen}
	<!-- svelte-ignore a11y_click_events_have_key_events -->
	<!-- svelte-ignore a11y_interactive_supports_focus -->
	<div 
		class="fixed inset-0 z-[100] flex items-center justify-center bg-black/80 backdrop-blur-sm"
		onclick={handleBackdropClick}
		role="dialog"
		aria-modal="true"
		aria-labelledby="modal-title"
	>
		<div class="relative w-full max-w-4xl mx-4 bg-white rounded-lg overflow-hidden">
			<!-- Close Button -->
			<button
				onclick={onClose}
				class="absolute top-6 right-6 z-10 text-gray-400 hover:text-black transition-colors"
				aria-label="Close modal"
			>
				<X size={24} />
			</button>

			<div class="grid md:grid-cols-2">
				<!-- Form Section -->
				<div class="p-12">
					<div class="mb-8">
						<p class="text-xs text-gray-500 mb-2 tracking-wide uppercase">Demo Request</p>
						<h2 id="modal-title" class="text-3xl font-medium mb-3 text-black">
							See DiligenceSquared in Action
						</h2>
						<p class="text-sm text-gray-600 leading-relaxed">
							Let us show you how we deliver investor-grade due diligence in days, not weeks.
						</p>
					</div>

					<form onsubmit={handleSubmit} class="space-y-5">
						<!-- Name Fields -->
						<div class="grid grid-cols-2 gap-4">
							<div>
								<label for="firstName" class="block text-xs text-gray-600 mb-2 font-medium">
									First Name
								</label>
								<input
									type="text"
									id="firstName"
									bind:value={formData.firstName}
									required
									class="w-full px-0 py-2 border-0 border-b border-gray-300 focus:border-black focus:outline-none transition-colors text-sm"
									placeholder="John"
								/>
							</div>
							<div>
								<label for="lastName" class="block text-xs text-gray-600 mb-2 font-medium">
									Last Name
								</label>
								<input
									type="text"
									id="lastName"
									bind:value={formData.lastName}
									required
									class="w-full px-0 py-2 border-0 border-b border-gray-300 focus:border-black focus:outline-none transition-colors text-sm"
									placeholder="Smith"
								/>
							</div>
						</div>

						<!-- Email -->
						<div>
							<label for="email" class="block text-xs text-gray-600 mb-2 font-medium">
								Business Email
							</label>
							<input
								type="email"
								id="email"
								bind:value={formData.email}
								required
								class="w-full px-0 py-2 border-0 border-b border-gray-300 focus:border-black focus:outline-none transition-colors text-sm"
								placeholder="john.smith@firm.com"
							/>
						</div>

						<!-- Firm and Title -->
						<div class="grid grid-cols-2 gap-4">
							<div>
								<label for="firm" class="block text-xs text-gray-600 mb-2 font-medium">
									Firm / Company
								</label>
								<input
									type="text"
									id="firm"
									bind:value={formData.firm}
									required
									class="w-full px-0 py-2 border-0 border-b border-gray-300 focus:border-black focus:outline-none transition-colors text-sm"
									placeholder="Acme Capital"
								/>
							</div>
							<div>
								<label for="title" class="block text-xs text-gray-600 mb-2 font-medium">
									Title
								</label>
								<input
									type="text"
									id="title"
									bind:value={formData.title}
									required
									class="w-full px-0 py-2 border-0 border-b border-gray-300 focus:border-black focus:outline-none transition-colors text-sm"
									placeholder="Principal"
								/>
							</div>
						</div>

						<!-- Phone -->
						<div>
							<label for="phone" class="block text-xs text-gray-600 mb-2 font-medium">
								Phone Number
							</label>
							<input
								type="tel"
								id="phone"
								bind:value={formData.phone}
								class="w-full px-0 py-2 border-0 border-b border-gray-300 focus:border-black focus:outline-none transition-colors text-sm text-black"
								placeholder="+1 (555) 123-4567"
							/>
						</div>

						<!-- Message -->
						<div>
							<label for="message" class="block text-xs text-gray-600 mb-2 font-medium">
								Tell us about your needs (optional)
							</label>
							<textarea
								id="message"
								bind:value={formData.message}
								rows="3"
								class="w-full px-0 py-2 border-0 border-b border-gray-300 focus:border-black focus:outline-none transition-colors text-sm resize-none text-black"
								placeholder="e.g., Looking for pre-LOI diligence support..."
							></textarea>
						</div>

						<!-- Submit Button -->
						<button
							type="submit"
							class="w-full bg-black text-white py-3 rounded text-sm font-medium hover:bg-gray-800 transition-colors mt-6"
						>
							Request Demo
						</button>
					</form>
				</div>

				<!-- Right Side - Visual/Content Section -->
				<div class="hidden md:block bg-gray-50 p-12 flex flex-col justify-center">
					<div class="space-y-8">
						<div>
							<h3 class="text-lg font-medium mb-2">What to Expect</h3>
							<ul class="space-y-3 text-sm text-gray-600">
								<li class="flex items-start gap-2">
									<span class="text-black mt-0.5">•</span>
									<span>30-minute personalized demo of the platform</span>
								</li>
								<li class="flex items-start gap-2">
									<span class="text-black mt-0.5">•</span>
									<span>See real interview transcripts and synthesis reports</span>
								</li>
								<li class="flex items-start gap-2">
									<span class="text-black mt-0.5">•</span>
									<span>Discuss your specific diligence needs</span>
								</li>
								<li class="flex items-start gap-2">
									<span class="text-black mt-0.5">•</span>
									<span>Learn about pricing and implementation timeline</span>
								</li>
							</ul>
						</div>

						<div class="pt-6 border-t border-gray-300">
							<p class="text-xs text-gray-500 mb-2">Trusted by leading PE firms</p>
							<p class="text-sm text-gray-700 italic">
								"80% of the insight at 5% of the cost, delivered in days, not weeks."
							</p>
							<p class="text-xs text-gray-500 mt-2">— Managing Director, Leading PE Fund</p>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
{/if}
