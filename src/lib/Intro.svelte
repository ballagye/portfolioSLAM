<script>
  import BgcLogo from "./components/BgcLogo.svelte";
</script>

<section class="intro">
  <div class="Typist">
    <div>
      <h1>Bonjour, Je m'appelle</h1>
    </div>
  </div>
  <div>
    <h2 class="big-heading">Balla Gueye.</h2>
  </div>

  <span class=" Cursor blinking-cursor"></span>
  <div class="intro-subtitle">Je développe des applications.</div>
  <div class="intro-desc">Je suis étudiant à l'efrei blablabla</div>
</section>
<div id="bgc-logo"><BgcLogo /></div>

<style>
  .intro {
    background-color: oklch(25.7% 0.09 281.288);
    margin: 202px;
  }

  div {
    display: block;
  }
  .Typist {
    font-weight: bold;
    font-family: "SF Pro Display", sans-serif;
    color: oklch(87% 0.065 274.039);
  }

  h1 {
    color: #6ecfff;
    font-size: clamp(var(--fz-sm), 5vw, var(--fz-md));
    font-weight: 400;
    font-family: "IBM Plex Mono", monospace;
  }

  h2 {
    font-family: "SF Pro Display", sans-serif;
    color: oklch(93% 0.034 272.788);
    line-height: 1.1;
  }
  .big-heading {
    font-weight: 900;
    margin: 0px;
    font-size: 96px;
  }
</style>
