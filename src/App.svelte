<script>
  import Intro from "./lib/Intro.svelte";
  import BtsSection from "./lib/components/BtsSection.svelte";
  import About from "./lib/components/About.svelte";
  import Experience from "./lib/components/Experience.svelte";
  import Experiencecopy from "./lib/components/Experience copy.svelte";
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
    <section><Experience /></section>
    <section><Experiencecopy /></section>
  </main>
</div>

<!-- c'est root! -->
