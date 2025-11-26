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
      personnes qui souhaitent se former en deux ans aux métiers d’<span
        class="colored"
        >administrateurs réseau
      </span>
      ou de <span class="colored">développeur</span>.
    </p>
    <br />
    <p>
      Il peut-être réalisable soit en <span class="colored">alternance </span>
      d’une durée de 12 ou de 24 ou alors en
      <span class="colored"> initial </span> un minimum de 10 semaines de stages
      obligatoire en entreprise d’une durée de 2 à 3 mois, afin de s’initier aux
      réalités du domaine professionnel.
    </p>
    <br />
    <p>
      <b
        >Le BTS SIO propose deux <span class="colored"> spécialités</span> :
      </b>
    </p>
  </div>
  <div class="sisr">
    <div class="sisr-content">
      <ul class="options-list">
        <li>
          Gestion des <span class="colored"> systèmes d’exploitation</span> et des
          services réseaux
        </li>
        <li>
          Gestion et la maintenance des infrastructures <span class="colored"
            >réseau</span
          >
        </li>
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
    font-size: 18px;
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
    position: relative;
    grid-column: 7 / 11;
    grid-row-start: 1;
    grid-row-end: -1;
  }
  .sisr-image {
    position: relative;
    grid-column: 2 / 8;
    grid-row-start: 1;
    grid-row-end: -1;
  }
  .options-list {
    background-color: var(--dark-indigo);
    position: relative;
    padding: 15px 47px;
    margin-left: -60px;
    z-index: 2;
    border-radius: 2px;
    font-family: var(--sfpro);
    color: var(--light-indigo2);
    font-weight: 400;
    font-size: 19px;
  }

  .bts-desc {
    margin-bottom: 111px;
  }
  .colored {
    color: var(--blue);
  }
</style>
