<script>
  import SectionHeader from "./SectionHeader.svelte";
  import MeImage from "./MeImage.svelte";
</script>

<section class="about-section">
  <div class="section-header">
    <SectionHeader title={"/ A propos"} />
  </div>
  <div class="inner">
    <div class="about">
      <p>Je suis <b>Balla Gueye</b>, étudiant en BTS SIO</p>
      <p>
        Au cours de mes deux années de formation, j’ai réalisé des stages
        concrets :
      </p>
      <p>
        Lors de ma première année, j’ai effectué un stage chez <b>Alstom</b>,
        dans le département Network & IT, où j’ai développé un logiciel pour
        automatiser les configurations réseaux sur des projets ferroviaires.
      </p>
      <p>
        Lors de ma deuxième année, j’ai travaillé chez <b>SAIGON</b>, où j’ai
        participé à l’amélioration du site web et migré la gestion des stocks
        d’Excel vers une solution en Java.
      </p>
      <ul class="tech-stack">
        <li>JavaScript</li>
        <li>Typescript</li>
        <li>Python</li>
        <li>Svelte</li>
        <li>Java</li>
        <li>Wordpress</li>
      </ul>
    </div>
    <div class="meimage"><MeImage /></div>
  </div>
</section>

<style>
  .about-section {
    margin: 0px auto;
    max-width: 1100px;
  }
  .section-header {
    display: flex;
    flex-direction: row;
    width: 100%;
    margin: 0px;
    padding: 0;
  }
  p {
    font-family: var(--sfpro);
    color: var(--light-indigo2);
    font-size: 17px;
  }
  .inner {
    display: flex;
  }
  .meimage {
    position: relative;
    max-width: 300px;
    padding-left: 40px;
  }
  .about {
    max-width: 600px;
  }
  .tech-stack {
    display: grid;
    grid-template-columns: repeat(2, minmax(140px, 200px));
    gap: 0px 10px;
    padding: 0px;
    margin: 20px 0px 0px;
    overflow: hidden;
    list-style: none;
    font-family: var(--ibm);
  }
  .tech-stack li::before {
    color: var(--blue);
    content: "▹";
    left: 0;
    position: absolute;
  }
  .tech-stack li {
    position: relative;
    margin-bottom: 10px;
    padding-left: 20px;
    font-family: var(--ibm);
    font-size: var(--fz-xs);
    color: var(--light-indigo2);
  }
</style>
