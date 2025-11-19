<script>
  import FractalTree from "./FractalTree.svelte";
</script>

<div id="intro">
  <div id="fractal-tree"><FractalTree /></div>

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
</div>

<style>
  #intro {
    display: flex;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    margin: auto;
    max-width: 1000px;
    padding-top: 200px;
    min-height: 100vh;
  }
</style>
