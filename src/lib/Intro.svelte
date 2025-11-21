<script>
  import BgcLogo from "./components/BgcLogo.svelte";
</script>

<div id="intro">
  <div id="bgc-logo"><BgcLogo /></div>

  <div class="Typist">
    <span class="intro-title">
      Bonjour, Je m'appelle
      <span class="intro-name">Balla Gueye.</span>
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
    font-weight: bold;
    font-family: "SF Pro Display", sans-serif;
    color: oklch(87% 0.065 274.039);
  }

  .intro-name {
    font-size: 96px;
    font-weight: 900;
    font-family: "SF Pro Display", sans-serif;

    color: #eef2ff;
  }
  .intro-title {
    font-weight: 300;
    font-family: "IBM Plex Mono", monospace;
    color: #6ecfff;
  }
  .intro-subtitle {
    color: #858fad;
    font-size: 80px;
  }
</style>
