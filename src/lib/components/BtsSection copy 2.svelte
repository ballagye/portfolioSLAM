<script>
  import SectionHeader from "./SectionHeader.svelte";
  import Images from "./Images.svelte";
</script>

<section id="bts-sio">
  <div class="section-header"><SectionHeader /></div>
  <div class="bts-desc">
    <p>
      Le Brevet de Technicien Supérieur aux Services Informatiques aux
      Organisations (BTS SIO) est un programme de niveau Bac+2 et s’adresse aux
      personnes qui souhaitent se former en deux ans aux métiers
      d’administrateurs réseau ou de développeur
    </p>
    <br />
    <p>
      Il peut-être réalisable soit en alternance d’une durée de 12 ou de 24 ou
      alors en initial avec un minimum de 10 semaines de stages obligatoire en
      entreprise d’une durée de 2 à 3 mois, afin de s’initier aux réalités du
      domaine professionnel.
    </p>
    <br />
    <p>Le BTS SIO propose deux spécialités :</p>
  </div>
  <div class="sisr">
    <div class="sisr-content">
      <ul class="options-list">
        <li>Gestion des systèmes d’exploitation et des services réseaux</li>
        <li>Gestion et la maintenance des infrastructures réseau</li>
        <li>Optimisation des performances d’un réseau</li>
        <li>Sécurisations des infrastructures</li>
      </ul>
    </div>
    <div class="sisr-image"><Images /></div>
  </div>
</section>

<style>
  p {
    margin: 0px 25px 0px 0px;
    font-family: "SF Pro Display", sans-serif;
    font-size: 400;
    color: oklch(96.2% 0.018 272.314);
    font-family: "SF Pro Display", sans-serif;
  }

  #bts-sio {
    margin: 150px;
  }
  .sisr {
    display: grid;
    align-items: center;
    gap: 10px;
    grid-template-columns: repeat(12, 1fr);
  }
  .sisr-content {
    grid-column: 7 / -1;
    grid-row-start: 1;
    grid-row-end: -1;
  }
  .sisr-image {
    grid-column: 1 / 8;
    grid-row-start: 1;
    grid-row-end: -1;
  }
  .options-list {
    background-color: var(--indigo-dark);
    position: relative;
    padding: 15px 47px;
    margin-left: -60px;
    z-index: 2;
    border-radius: 2px;
  }

  section {
    padding: 150px;
  }
</style>
