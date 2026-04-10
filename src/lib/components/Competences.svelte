<script>
  import SectionHeader from "./SectionHeader.svelte";
</script>

<div class="competences">
  <h1>Réalisations professionnelles</h1>
  <ul>
    <li>
      <h1>Bloc 1</h1>
      <p>Gérer le patrimoine informatique</p>
      <a href="#experience">
        <video
          src="/glpi-showcase.mp4"
          muted
          autoplay
          loop
          playsinline
          width="660px"
        >
        </video>
      </a>
    </li>
    <li>
      <h1>Bloc 2</h1>
      <p>Gérer le patrimoine informatique</p>
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

<style>
  h1,
  p {
    margin: 5px;
    font-family: var(--sfpro);
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
