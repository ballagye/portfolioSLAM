<script>
  import SectionHeader from "./SectionHeader.svelte";
</script>

<div class="section-header"><SectionHeader /></div>
<div class="bts-desc">
  <p>
    Le Brevet de Technicien Supérieur aux Services Informatiques aux
    Organisations (BTS SIO) est un programme de niveau Bac+2 et s’adresse aux
    personnes qui souhaitent se former en deux ans aux métiers d’administrateurs
    réseau ou de développeur
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

<ul class="sisr-slam">
  <li class="sisr-section">
    <div class="sisr-content">
      <div>
        <p class="sisr-overline">SISR</p>
        <h3 class="sisr-title">Réseaux</h3>
      </div>
      <div class="sisr-image"></div>
    </div>
  </li>
  <div class="sisr-description">
    <ul>
      <li>Gestion des systèmes d’exploitation et des services réseaux</li>
      <li>Gestion et la maintenance des infrastructures réseau</li>
      <li>Optimisation des performances d’un réseau</li>
      <li>Sécurisations des infrastructures</li>
    </ul>
  </div>
  <div>
    <ul class="sisr-tech-list">
      <li>Machines Virtuelles</li>
      <li>Linux</li>
      <li>Windows Server</li>
    </ul>
  </div>
</ul>

<style>
  .bts-desc {
    display: flex;
    flex-direction: column;
    margin: 0px 202px;
  }

  p {
    margin: 0px 25px 0px 25px;
    font-family: "SF Pro Display", sans-serif;
    font-size: 400;
    color: oklch(96.2% 0.018 272.314);
    font-family: "SF Pro Display", sans-serif;
  }
  .sisr-description {
    box-shadow: 0 10px 30px -15px var(--navy-shadow);
    transition: var(--transition);
    position: relative;
    z-index: 2;
    padding: 25px;
    border-radius: var(--border-radius);
    background-color: var(--indigo-dark);
    color: var(--light-slate);
    font-size: var(--fz-lg);
  }
  .sisr-content {
    grid-column: 7 / -1;
    text-align: right;
  }
</style>
