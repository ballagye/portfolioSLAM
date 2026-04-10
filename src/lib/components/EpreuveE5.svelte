<script>
  import SectionHeader from "./SectionHeader.svelte";
</script>

<section id="e5">
  <SectionHeader
    title={"/ Epreuve E5 : Support et mise à disposition de services informatiques"}
  />
  <div class="e5-presentation">
    <p>
      Cette épreuve vise à évaluer chez la personne candidate l’acquisition des
      compétences dans le cadre du "Support et mise à disposition de services
      informatiques".
    </p>
    <h3>Modalité d'évaluation</h3>
    <ul>
      <li>Durée 40 minutes</li>
      <li>Coefficient : 4</li>
      <li>Présentation de 10 minutes du parcours de professionnalisation</li>
      <li>
        Entretien de 30 minutes avec le jury pour approfondir les réalisations
      </li>
    </ul>
  </div>
</section>

<style>
  .e5-presentation {
    display: flex;
    flex-direction: column;
  }

  h3 {
    font-family: var(--ibm);
    color: var(--blue);
    font-size: 18px;
    font-weight: 400;
  }

  p {
    font-family: var(--sfpro);
  }

  #e5 {
    margin: 0px auto;
    max-width: 1300px;
  }

  ul {
    font-family: var(--ibm);
    color: var(--light-indigo2);
    list-style: none;
    max-width: 800px;
    font-size: 18px;
    padding: 0px;
  }

  ul li {
    position: relative;
    margin-bottom: 10px;
    padding-left: 30px;
  }

  li::before {
    content: "▹";
    position: absolute;
    left: -2px;
    color: var(--blue);
  }
</style>
