<section class="hero relative flex min-h-[90vh] items-center justify-center overflow-hidden px-4 py-12">
	<!-- Animated background elements -->
	<div class="pointer-events-none absolute -right-24 -top-24 h-72 w-72 rounded-full bg-primary/20 blur-3xl animate-pulse"></div>
	<div class="pointer-events-none absolute -bottom-24 left-10 h-64 w-64 rounded-full bg-accent/20 blur-3xl animate-pulse" style="animation-delay: 1s;"></div>
	<div class="pointer-events-none absolute right-1/4 top-1/3 h-48 w-48 rounded-full bg-primary/10 blur-2xl animate-pulse" style="animation-delay: 2s;"></div>
	
	<!-- Subtle grid pattern overlay -->
	<div class="absolute inset-0 opacity-[0.02]" style="background-image: linear-gradient(rgba(255,255,255,0.05) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.05) 1px, transparent 1px); background-size: 50px 50px;"></div>
	
	<div class="relative z-10 w-full max-w-4xl animate-fade-in">
		<div class="flex flex-col gap-8 text-left">
			<div class="text-text animate-slide-up">
				<h1 class="text-3xl font-bold leading-tight sm:text-4xl md:text-5xl tracking-tight">
					Being <span class="text-primary">creative</span>
					<span class="text-secondary font-normal"> and</span> making
					<span class="block mt-2">something <span class="text-accent">awesome</span>.</span>
				</h1>
			</div>
			
			<div class="flex flex-col gap-6 animate-slide-up" style="animation-delay: 0.1s;">
				<p class="text-base leading-relaxed text-text sm:text-lg md:text-xl max-w-2xl">
					<span class="font-bold text-primary">British Model College Hack Club</span> is where
					beginners and veterans come together to learn, teach, and build cool stuff. We're not just a
					coding club but a <span class="text-accent font-semibold">space where mistakes are celebrated</span>, questions are encouraged, and everyone
					grows together.
				</p>
				<p class="text-base leading-relaxed text-text sm:text-lg md:text-xl max-w-2xl">
					Whether you want to build your first website, create a game, dive into AI, or just figure out
					what programming even is, there's a place for you here. <span class="text-text font-semibold">No experience required.</span> Just bring
					your curiosity.
				</p>
			</div>
			
			<div class="flex flex-wrap items-center gap-4 pt-4 animate-slide-up" style="animation-delay: 0.2s;">
				<a
					href="/about"
					class="rounded-full bg-primary px-8 py-3.5 text-sm font-bold text-white transition-all duration-300 hover:scale-105 hover:shadow-lg hover:shadow-primary/50 hover:bg-primary/90"
				>
					Learn More
				</a>
				<a
					href="/contact"
					class="group relative overflow-hidden rounded-full border-2 border-primary/60 px-8 py-3.5 text-sm font-bold text-text backdrop-blur-sm transition-all duration-300 hover:scale-105 hover:border-primary hover:bg-primary/10 hover:shadow-lg hover:shadow-primary/30"
				>
					<span class="relative z-10">Get in Touch</span>
				</a>
			</div>
		
		</div>
	</div>
</section>

<style>
	@keyframes fade-in {
		from {
			opacity: 0;
		}
		to {
			opacity: 1;
		}
	}

	@keyframes slide-up {
		from {
			opacity: 0;
			transform: translateY(30px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	.animate-fade-in {
		animation: fade-in 0.8s ease-out forwards;
		opacity: 0;
	}

	.animate-slide-up {
		animation: slide-up 0.8s ease-out forwards;
		opacity: 0;
	}

	/* Smooth scrolling for better UX */
	:global(html) {
		scroll-behavior: smooth;
	}
</style>
