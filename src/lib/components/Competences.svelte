<script lang="ts">
  import { Router, Link, Route } from "svelte5-router";
  import { sineOut } from "svelte/easing";
  import { onMount } from "svelte";
  import { fly } from "svelte/transition";
  import Bloc1 from "../../routes/Bloc1.svelte";
  import Bloc2 from "../../routes/Bloc2.svelte";
  import Bloc3 from "../../routes/Bloc3.svelte";
  import Bloc4 from "../../routes/Bloc4.svelte";
  import Bloc5 from "../../routes/Bloc5.svelte";
  import Bloc6 from "../../routes/Bloc6.svelte";
  import SectionHeader from "./SectionHeader.svelte";

  let url = $state("");

  let competences: HTMLElement | null = null;

  onMount(() => {
    if (!competences) return;
    const observer = new IntersectionObserver(() => {});
    observer.observe(competences);
    return () => observer.disconnect();
  });
</script>

<Router {url}>
  <div class="competences">
    <h1>Réalisations professionnelles</h1>
    <ul>
      <li>
        <h1>Bloc 1</h1>
        <p>Gérer le patrimoine informatique</p>
        <Link to="/Bloc1">
          <video
            src="/glpi-showcase.mp4"
            muted
            autoplay
            loop
            playsinline
            width="660px"
          >
          </video>
        </Link>
      </li>
      <li transition:fly={{ y: 100, duration: 700, easing: sineOut }}>
        <h1>Bloc 2</h1>
        <p>
          Répondre aux incidents et aux demandes d’assistance et d’évolution
        </p>
        <Link to="/Bloc2">
          <video
            src="/ticket showcase.mp4"
            muted
            autoplay
            loop
            playsinline
            width="660px"
          >
          </video>
        </Link>
      </li>
      <li>
        <h1>Bloc 3</h1>
        <p>Développer la présence en ligne de l’organisation</p>
        <Link to="/Bloc3">
          <video
            src="/identite-num.mp4"
            muted
            autoplay
            loop
            playsinline
            width="660px"
          >
          </video>
        </Link>
      </li>
      <li>
        <h1>Bloc 4</h1>
        <p>Travailler en mode projet</p>
        <Link to="/Bloc4">
          <video src="/grafana.mp4" muted autoplay loop playsinline width="660px">
          </video>
        </Link>
      </li>
      <li>
        <h1>Bloc 5</h1>
        <p>Mettre à disposition des utilisateurs un service informatique</p>
        <Link to="/Bloc5">
          <video src="/service-video.mp4" muted autoplay loop playsinline width="660px">
          </video>
        </Link>
      </li>
      <li>
        <h1>Bloc 6</h1>
        <p>Organiser son développement professionnel</p>
        <Link to="/Bloc6">
          <video src="/notion-video.mp4" muted autoplay loop playsinline width="660px">
          </video>
        </Link>
      </li>
    </ul>
  </div>
  <Route path="/Bloc1" component={Bloc1} />
  <Route path="/Bloc2" component={Bloc2} />
  <Route path="/Bloc3" component={Bloc3} />
  <Route path="/Bloc4" component={Bloc4} />
  <Route path="/Bloc5" component={Bloc5} />
  <Route path="/Bloc6" component={Bloc6} />
</Router>

<style>
  h1,
  p {
    margin: 5px;
    font-family: var(--sfpro);
  }
  p {
    color: var(--blue);
  }

  li {
    list-style: none;
    width: 660px;
  }
  video {
    border-radius: 4px;
  }
  ul {
    display: grid;
    grid-template-columns: repeat(2, 660px);
    row-gap: 40px;
    column-gap: 24px;
    justify-content: center;
  }
  .competences {
    margin: 0px auto;
    max-width: 1310px;
  }
</style>
