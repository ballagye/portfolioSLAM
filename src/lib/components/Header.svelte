<script lang="ts">
  const header = [
    "BTS",
    "A propos",
    "Expérience",
    "Epreuves",
    "Veille Technologique",
  ];
</script>

<header>
  <nav>
    <h1>Balla Gueye</h1>
    <ul>
      {#each header as headers}
        <li>{headers}</li>
      {/each}
      <a class="cv-button" href="./cv.pdf" target="_blank">CV</a>
    </ul>
  </nav>
</header>

<style>
  header {
    display: flex;
    -webkit-box-pack: justify;
    justify-content: space-between;
    -webkit-box-align: center;
    align-items: center;
    position: fixed;
    top: 0px;
    z-index: 11;
    padding: 0px 10px 0px 50px;
    width: 100%;
    height: var(--nav-height);
    background-color: var(--indigo);
    backdrop-filter: blur(140px);
    transition: var(--transition);
    filter: none !important;
    pointer-events: auto !important;
    user-select: auto !important;
  }
  nav {
    display: flex;
    -webkit-box-pack: justify;
    justify-content: space-between;
    backdrop-filter: blur(1000px);
    -webkit-box-align: center;
    align-items: center;
    position: relative;
    width: 100%;
    color: var(--light-indigo2);
    font-family: var(--ibm);
    z-index: 12;
  }
  h1 {
    font-family: var(--sfpro);
    color: var(--light-indigo);
  }
  ul {
    display: flex;
    -webkit-box-align: center;
    gap: 40px;
    align-items: center;
    list-style: none;
    padding: 0rem 5rem 0rem 2rem;
  }
  .cv-button {
    color: var(--blue);
    background-color: transparent;
    border: 1px solid var(--blue);
    border-radius: var(--border-radius);
    padding: 0.75rem 1rem;
    font-family: var(--font-mono);
    line-height: 1;
    text-decoration: none;
    transition: var(--transition);
    margin-left: 15px;
    font-size: var(--fz-xs);
  }
  .cv-button:hover {
    outline: none;
    box-shadow: 3px 3px 0 0 var(--blue);
    transform: translate(-4px, -4px);
  }
</style>
