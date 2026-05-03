<script lang="ts">
  import { Router, Link, Route } from "svelte5-router";
  import { sineOut } from "svelte/easing";
  import { onMount } from "svelte";
  import { fly } from "svelte/transition";
  import Bloc1 from "../../routes/Bloc1.svelte";
  import SectionHeader from "./SectionHeader.svelte";

  let url = $state("");

  let competences: HTMLElement | null = null;
  let visible = false;

  onMount(() => {
    if (!competences) return;
    const observer = new IntersectionObserver((entries) => {
      const entry = entries[0];
      if (entry.isIntersecting) {
        visible = true;
      }
    });
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
        <video
          src="/ticket showcase.mp4"
          muted
          autoplay
          loop
          playsinline
          width="660px"
        >
        </video>
      </li>
      <li>
        <h1>Bloc 3</h1>
        <p>Développer la présence en ligne de l’organisation</p>
        <video
          src="/identite-num.mp4"
          muted
          autoplay
          loop
          playsinline
          width="660px"
        >
        </video>
      </li>
      <li>
        <h1>Bloc 4</h1>
        <p>Travailler en mode projet</p>
        <video src="/grafana.mp4" muted autoplay loop playsinline width="660px">
        </video>
      </li>
    </ul>
  </div>
  <Route path="/Bloc1" component={Bloc1} />
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
