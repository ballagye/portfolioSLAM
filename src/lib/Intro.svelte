<script>
  import BgcLogo from "./components/BgcLogo.svelte";
</script>

<div id="intro">
  <div class="Typist">
    <div id="intro-text">
      <p>Bonjour, je m'appelle</p>
      <h1 class="big-heading">Balla Gueye.</h1>
      <h2 class="big-heading">Étudiant en BTS SIO à l'EFREI.</h2>
      <p class="intro-subtitle">
        Je développe des logiciels et automatise le déploiement de
        configurations ou des services, précédemment stagiaire à Alstom &
        SAIGON.
      </p>
    </div>
  </div>
  <div id="bgc-logo"><BgcLogo /></div>
  <span class=" Cursor blinking-cursor"></span>
</div>

<style>
  #intro {
    background-color: oklch(25.7% 0.09 281.288);
    margin: auto;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap-reverse;
    padding: 0;
    justify-content: center;
    align-items: center;
    padding: 15em 0em 12em;
  }

  div {
    display: block;
  }
  .Typist {
    font-weight: bold;
    font-family: "SF Pro Display", sans-serif;
    color: oklch(87% 0.065 274.039);
  }
  p {
    color: #6ecfff;
    font-size: clamp(var(--fz-sm), 5vw, var(--fz-md));
    font-weight: 400;
    font-family: "IBM Plex Mono", monospace;
    margin-left: 3px;
  }
  h1 {
    font-family: "SF Pro Display", sans-serif;
    color: oklch(93% 0.034 272.788);
    line-height: 1.1;
    font-weight: 900;
    margin: 0px;
    font-size: 96px;
    line-height: 1.1;
  }

  h2 {
    margin: 0;
    font-size: 65px;
    font-family: "SF Pro Display", sans-serif;
    color: #858fad;
    line-height: 1.3;
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
