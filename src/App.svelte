<script>
  import Intro from "./lib/Intro.svelte";
  import BtsSection from "./lib/components/BtsSection.svelte";
  import About from "./lib/components/About.svelte";
  import Experience from "./lib/components/Experience.svelte";
  import Header from "./lib/components/Header.svelte";
  import Footer from "./lib/components/Footer.svelte";
</script>

<div id="root">
  <header><Header /></header>
  <main class="App">
    <section id="intro">
      <div><Intro /></div>
    </section>
    <section id="bts-sio">
      <div><BtsSection /></div>
    </section>
    <section id="about">
      <div><About /></div>
    </section>
    <section id="experience"><Experience /></section>
  </main>
  <footer><Footer /></footer>
</div>

<style>
  section {
    padding: 100px 0px;
    margin: 0px auto;
  }
</style>
