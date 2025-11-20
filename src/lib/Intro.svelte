<script>
  import FractalTree from "./FractalTree.svelte";
</script>

<div id="intro">
  <div id="fractal-tree"><FractalTree /></div>

  <div class="Typist">
    <span class="intro-title">
      Bonjour, Je m'appelle
      <span class="intro-name">Balla</span>
    </span>
    <span class=" Cursor blinking-cursor"></span>
    <div class="intro-subtitle">Je développe des applications.</div>
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
    max-width: 1500px;
    padding-top: 200px;
    min-height: 100vh;
  }
  .Typist {
    font-size: 76px;
    color: oklch(87% 0.065 274.039);
    font-family:
      system-ui,
      -apple-system,
      BlinkMacSystemFont,
      "Segoe UI",
      "Open Sans",
      "Helvetica Neue",
      sans-serif;
  }

  .intro-name {
    color: #6ecfff;
  }
  .intro-title {
    font-weight: bold;
  }
  .intro-subtitle {
    color: #858fad;
    font-size: 80px;
  }
</style>
