<script>
  import SectionHeader from "./lib/components/SectionHeader.svelte";
  import Intro from "./lib/Intro.svelte";
  import BtsSection from "./lib/components/BtsSection.svelte";
  import BtsSectioncopy from "./lib/components/BtsSection copy.svelte";
</script>

<div id="root">
  <main class="App">
    <section class="intro">
      <div id="intro"><Intro /></div>
    </section>
    <section class="bts-sio">
      <div id="bts-sio"><BtsSection /></div>
    </section>
    <section><BtsSectioncopy /></section>
    <div class="about-content">
      <div class="about-description">
        <p></p>
        text blablabla
        <ul></ul>
      </div>
    </div>
    <div id="experience">
      <!-- Je m'en occupe plus tard -->
      <div class="section-header">
        <span class="section-title"> / éxpérience</span>
      </div>
    </div>
    <div id="bts-sio">
      <!-- Je m'en occupe plus tard -->
      <div class="section-header">
        <span class="section-title"> / BTS SIO</span>
      </div>
    </div>
    <div id="projets">
      <div class="section-header"></div>
      <!-- Je m'en occupe plus tard -->
    </div>
  </main>
</div>

<!-- c'est root! -->

<style>
</style>
