<script>
  import "../app.css";
  import Footer from "../components/Footer.svelte";
  import Hero from "../components/Hero.svelte";
  import Navbar from "../components/Navbar.svelte";
  import Pricing from "../components/Pricing.svelte";
  import TariffCalculator from "../components/TariffCalculator.svelte";
</script>

<div class="app">
  <!-- <Header />

  <main>
    <slot />
  </main>

  <footer>
    <p>
      visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit
    </p>
  </footer> -->

  <Navbar />
  <Hero />

  <TariffCalculator />

  <Pricing />
  <Footer />
</div>

<style>
</style>
