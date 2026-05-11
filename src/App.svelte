<script>
  import { Router, Route } from "svelte5-router";
  import Bloc1 from "./routes/Bloc1.svelte";
  import Bloc2 from "./routes/Bloc2.svelte";
  import Bloc3 from "./routes/Bloc3.svelte";
  import Bloc4 from "./routes/Bloc4.svelte";
  import Bloc5 from "./routes/Bloc5.svelte";
  import Bloc6 from "./routes/Bloc6.svelte";
  import Intro from "./lib/Intro.svelte";
  import BtsSection from "./lib/components/BtsSection.svelte";
  import About from "./lib/components/About.svelte";
  import Experience from "./lib/components/Experience.svelte";
  import Header from "./lib/components/Header.svelte";
  import Footer from "./lib/components/Footer.svelte";
  import EpreuveE5 from "./lib/components/EpreuveE5.svelte";
  import Veille from "./routes/Veille.svelte";
  import EpreuveE6 from "./lib/components/EpreuveE6.svelte";
  import Projets from "./routes/Projets.svelte";
</script>

<Router>
  <Route path="/Bloc1" component={Bloc1} />
  <Route path="/Bloc2" component={Bloc2} />
  <Route path="/Bloc3" component={Bloc3} />
  <Route path="/Bloc4" component={Bloc4} />
  <Route path="/Bloc5" component={Bloc5} />
  <Route path="/Bloc6" component={Bloc6} />
  <Route path="/Veille" component={Veille} />
  <Route path="/Projets" component={Projets} />

  <Route path="/">
    <div id="root">
      <header><Header /></header>
      <main class="App">
        <section id="intro">
          <div><Intro /></div>
          <section id="about">
            <div><About /></div>
          </section>
          <section id="bts-sio">
            <div><BtsSection /></div>
          </section>
        </section>

        <section id="experience"><Experience /></section>
        <section id="e5"><EpreuveE5 /></section>
        <section id="e6"><EpreuveE6 /></section>
        <section id="projets"><Projets /></section>
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
