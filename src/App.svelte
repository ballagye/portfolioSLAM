<script>
  import Intro from "./lib/Intro.svelte";
</script>

<div id="root">
  <div class="App">
    <div id="intro"><Intro /></div>

    <div class="Typist">
      <span class="intro-title">
        Bonjour, Je m'appelle
        <span class="intro-name">Balla</span>
        .
      </span>
      <span class="Blinking Cursor"></span>
      <div class="intro-subtitle">I create stuff sometimes.</div>
      <div class="intro-desc">Je suis étudiant à l'efrei blablabla</div>
    </div>

    <div class="section-header">
      <span class="section-title"> / a propos</span>
    </div>
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
  </div>
</div>

<!-- c'est root! -->
