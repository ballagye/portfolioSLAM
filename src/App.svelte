<script>
  import Intro from "./lib/Intro.svelte";
  import BtsSection from "./lib/components/BtsSection.svelte";
  import About from "./lib/components/About.svelte";
</script>

<div id="root">
  <main class="App">
    <section class="intro">
      <div id="intro"><Intro /></div>
    </section>
    <section class="bts-sio">
      <div id="bts-sio"><BtsSection /></div>
    </section>
    <section>
      <div><About /></div>
    </section>
  </main>
</div>

<!-- c'est root! -->
