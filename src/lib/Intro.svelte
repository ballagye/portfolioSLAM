<script lang="ts">
  import BgcLogo from "./components/BgcLogo.svelte";
</script>

<section>
  <div id="intro">
    <div id="intro-text">
      <p>Bonjour, je m'appelle</p>
      <h1 class="big-heading">Balla Gueye.</h1>
      <h2 class="big-heading">Étudiant en BTS SIO à l'EFREI.</h2>
      <p class="intro-subtitle">
        Je développe des logiciels et automatise le déploiement de
        configurations ou des services, anciennement stagiaire chez Alstom et
        SAIGON.
      </p>
      <a href="mailto:ballagyepro@gmail.com" class="intro-contact"> Contact</a>
    </div>

    <div id="bgc-logo"><BgcLogo /></div>
  </div>
</section>

<style>
  #intro {
    margin: auto;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap-reverse;
    padding: 0;
    justify-content: center;
    align-items: center;
    padding: 10em 0em 0em;
  }

  div {
    display: block;
  }
  p {
    color: #6ecfff;
    font-size: clamp(var(--fz-sm), 5vw, var(--fz-md));
    font-weight: 300;
    font-family: "IBM Plex Mono", monospace;
    margin-left: 3px;
  }
  h1 {
    font-family: "SF Pro Display", sans-serif;
    color: var(--light-indigo);
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
    font-weight: 400;
    margin: 20px 0px 0px;
    max-width: 390px;
  }
  .intro-contact {
    display: inline-block;
    color: var(--blue);
    background-color: transparent;
    border: 1px solid var(--blue);
    border-radius: var(--border-radius);
    padding: 1rem 3rem;
    font-family: var(--ibm);
    text-decoration: none;
    transition: var(--transition);
    margin-top: 50px;
    font-weight: 400;
    line-height: 1;
  }
  .intro-contact:hover {
    outline: none;
    box-shadow: 4px 4px 0 0 var(--blue);
    transform: translate(-5px, -5px);
  }
</style>
