<script lang="ts">
  let mobileMenuOpen = $state(false);

  function toggleMenu() {
    mobileMenuOpen = !mobileMenuOpen;
  }
</script>

<nav class="fixed top-0 z-50 w-full border-b border-white/10 bg-background/90 backdrop-blur-xl">
  <div class="mx-auto flex h-20 max-w-7xl items-center justify-between px-4 sm:px-6 lg:px-8">
    <!-- Logo/Brand -->
    <a href="/" class="group flex items-center gap-3 transition-transform duration-300 hover:scale-105">
      <div class="relative">
        <div class="absolute inset-0 rounded-xl bg-primary/20 blur-md opacity-0 transition-opacity duration-300 group-hover:opacity-100"></div>
        <img
          src="/images/logo.png"
          alt="BMCHC logo"
          class="relative h-11 w-11 rounded-xl object-contain transition-all duration-300 sm:h-12 sm:w-12"
        />
      </div>
      <span class="text-lg font-bold tracking-tight text-text sm:text-xl">BMCHC</span>
    </a>

    <!-- Desktop Navigation -->
    <div class="hidden items-center gap-1 md:flex lg:gap-2">
      <a href="#home" class="nav-link">Home</a>
      <a href="#about" class="nav-link">About</a>
      <a href="#gallery" class="nav-link">Gallery</a>
      <a href="#contact" class="nav-link">Contact</a>
    </div>

    <!-- Desktop CTA -->
    <a
      href="https://bmchc.fillout.com/join" 
      target="_blank"
      class="hidden items-center gap-2 rounded-full bg-primary px-6 py-2.5 text-sm font-bold text-white shadow-lg shadow-primary/25 transition-all duration-300 hover:scale-105 hover:bg-primary/90 hover:shadow-xl hover:shadow-primary/40 md:inline-flex"
    >
      <span>Join Club</span>
      <svg class="h-4 w-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"></path>
      </svg>
    </a>

    <!-- Mobile Menu Button -->
    <button
      class="group relative flex h-10 w-10 items-center justify-center rounded-lg transition-colors hover:bg-white/5 md:hidden"
      aria-label="Toggle navigation"
      onclick={toggleMenu}
    >
      <span class="relative flex h-5 w-6 flex-col items-center justify-center gap-1.5">
        <span class="menu-line h-0.5 w-full rounded-full bg-text transition-all duration-300" class:menu-open={mobileMenuOpen}></span>
        <span class="menu-line h-0.5 w-full rounded-full bg-text transition-all duration-300" class:menu-open={mobileMenuOpen}></span>
        <span class="menu-line h-0.5 w-full rounded-full bg-text transition-all duration-300" class:menu-open={mobileMenuOpen}></span>
      </span>
    </button>
  </div>

  <!-- Mobile Menu -->
  <div class="mobile-menu fixed left-0 right-0 top-20 max-h-0 overflow-hidden border-b border-white/0 bg-elevated/95 backdrop-blur-xl transition-all duration-300 ease-in-out md:hidden" class:menu-open={mobileMenuOpen}>
    <div class="mx-auto max-w-7xl px-4 py-0 opacity-0 transition-opacity duration-300 sm:px-6">
      <div class="flex flex-col gap-1 py-4">
        <a href="#home" class="mobile-nav-link">
          <svg class="h-5 w-5 text-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path>
          </svg>
          <span>Home</span>
        </a>
        <a href="#about" class="mobile-nav-link">
          <svg class="h-5 w-5 text-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
          </svg>
          <span>About</span>
        </a>
        <a href="#gallery" class="mobile-nav-link">
          <svg class="h-5 w-5 text-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
          </svg>
          <span>Gallery</span>
        </a>
        <a href="#contact" class="mobile-nav-link">
          <svg class="h-5 w-5 text-accent" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
          </svg>
          <span>Contact</span>
        </a>
        <div class="mt-3 pt-3 border-t border-white/10">
          <a 
            href="https://bmchc.fillout.com/join" 
            target="_blank"
            class="flex items-center justify-center gap-2 rounded-xl bg-primary px-6 py-3.5 text-base font-bold text-white shadow-lg shadow-primary/30 transition-all duration-300 hover:bg-primary/90"
          >
            <span>Join Club</span>
            <svg class="h-5 w-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"></path>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </div>
</nav>

<style>
  .nav-link {
    position: relative;
    padding: 0.625rem 1rem;
    font-size: 0.9375rem;
    font-weight: 600;
    color: var(--color-secondary);
    transition: all 0.3s ease;
    border-radius: 0.75rem;
  }

  .nav-link:hover {
    color: var(--color-text);
    background-color: rgba(255, 255, 255, 0.05);
  }

  .nav-link::after {
    content: '';
    position: absolute;
    bottom: 0.25rem;
    left: 50%;
    width: 0;
    height: 2px;
    background-color: var(--color-primary);
    transform: translateX(-50%);
    transition: width 0.3s ease;
  }

  .nav-link:hover::after {
    width: 50%;
  }

  .mobile-nav-link {
    display: flex;
    align-items: center;
    gap: 0.875rem;
    padding: 1rem;
    font-size: 1rem;
    font-weight: 600;
    color: var(--color-secondary);
    border-radius: 0.75rem;
    transition: all 0.3s ease;
  }

  .mobile-nav-link:hover {
    color: var(--color-text);
    background-color: rgba(255, 255, 255, 0.08);
    transform: translateX(0.25rem);
  }

  /* Mobile menu animations */
  .mobile-menu.menu-open {
    max-height: 500px;
    border-bottom-color: rgba(255, 255, 255, 0.1);
  }

  .mobile-menu.menu-open > div {
    opacity: 1;
    padding-top: 0;
    padding-bottom: 0;
  }

  /* Hamburger animation */
  .menu-line.menu-open:nth-child(1) {
    transform: translateY(5px) rotate(45deg);
  }

  .menu-line.menu-open:nth-child(2) {
    opacity: 0;
    transform: translateX(-100%);
  }

  .menu-line.menu-open:nth-child(3) {
    transform: translateY(-5px) rotate(-45deg);
  }

  /* Add padding to body to account for fixed navbar */
  :global(body) {
    padding-top: 5rem;
  }
</style>
