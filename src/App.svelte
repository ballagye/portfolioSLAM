<script>
  import { Router, Route } from "svelte5-router";
  import Bloc1 from "./routes/Bloc1.svelte";
  import Intro from "./lib/Intro.svelte";
  import BtsSection from "./lib/components/BtsSection.svelte";
  import About from "./lib/components/About.svelte";
  import Experience from "./lib/components/Experience.svelte";
  import Header from "./lib/components/Header.svelte";
  import Footer from "./lib/components/Footer.svelte";
  import EpreuveE5 from "./lib/components/EpreuveE5.svelte";
  import Veille from "./routes/Veille.svelte";
</script>

<Router>
  <Route path="/Bloc1" component={Bloc1} />
  <Route path="/Veille" component={Veille} />

  <Route path="/">
    <div id="root">
      <header><Header /></header>
      <main class="App">
        <section id="intro">
          <div><Intro /></div>
          <section id="bts-sio">
            <div><BtsSection /></div>
          </section>
        </section>
        <section id="about">
          <div><About /></div>
        </section>
        <section id="experience"><Experience /></section>
        <section id="e5"><EpreuveE5 /></section>
      </main>
      <footer><Footer /></footer>
    </div>
  </Route>
</Router>

<style>
  section {
    padding: 100px 0px;
    margin: 0px auto;
  }
</style>
