<script>
  import Intro from "./lib/Intro.svelte";
  import BtsSection from "./lib/components/BtsSection.svelte";
  import About from "./lib/components/About.svelte";
  import Experience from "./lib/components/Experience.svelte";
  import Header from "./lib/components/Header.svelte";
</script>

<div id="root">
  <header><Header /></header>
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
  </main>
</div>

<style>
  section {
    padding: 100px 0px;
    margin: 0px auto;
  }
</style>
