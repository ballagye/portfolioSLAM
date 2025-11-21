<script>
  import BgcLogo from "./components/BgcLogo.svelte";
</script>

<section class="intro">
  <div class="Typist">
    <div id="intro-text">
      <h1>Bonjour, Je m'appelle</h1>
      <h2 class="big-heading">Balla Gueye.</h2>
      <h3 class="big-heading">Étudiant en BTS SIO à l'EFREI.</h3>
      <p class="intro-subtitle">
        Je développe des logiciels et automatise le déploiement de
        configurations ou des services. précédemment stagiaire Alstom & SAIGON.
      </p>
    </div>
  </div>

  <div id="bgc-logo"><BgcLogo /></div>
  <span class=" Cursor blinking-cursor"></span>
</section>

<style>
  .intro {
    background-color: oklch(25.7% 0.09 281.288);
    margin: 202px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap-reverse;
    padding: 0;
    justify-content: center;
    align-items: center;
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
  h3.big-heading {
    font-size: 65px;
    font-family: "SF Pro Display", sans-serif;
    color: #858fad;
    line-height: 1.1;
  }
  .big-heading {
    font-weight: 900;
    margin: 0px;
    font-size: 96px;
  }

  .intro-subtitle {
    font-size: larger;
    color: #858fad;
    font-family: "SF Pro Display", sans-serif;
    font-weight: 500;
    margin: 20px 0px 0px;
    max-width: 390px;
  }
</style>
