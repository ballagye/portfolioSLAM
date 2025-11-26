<script>
  import SectionHeader from "./SectionHeader.svelte";
  import Images from "./Images.svelte";
  import { Server } from "@lucide/svelte";
  import { Network } from "@lucide/svelte";
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
      <div>
        <p class="overline">SISR</p>
        <h3 class="option-title">Réseaux</h3>
        <ul class="options-list">
          <li>
            Gestion des <span class="colored"> systèmes d’exploitation</span> et
            des services réseaux
          </li>
          <li>
            Gestion et la maintenance des infrastructures <span class="colored"
              >réseau</span
            >
          </li>
          <li>Optimisation des performances d’un réseau</li>
          <li>Sécurisations des infrastructures</li>
        </ul>
        <ul class="sisr-tech-list">
          <li>Machine Virtuelles</li>
          <li>Linux</li>
          <li>Debian</li>
          <li>Ubuntu</li>
          <li>Windows Server</li>
        </ul>
        <div class="sisr-logo"><Server /> <Network /></div>
      </div>
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
    margin: 0px auto;
    max-width: 1100px;
  }
  .sisr {
    display: grid;
    align-items: center;
    justify-content: center;
    gap: 10px;
    grid-template-columns: repeat(12, 1fr);
  }
  .sisr-content {
    position: relative;
    grid-column: 7 / -1;
    grid-row-start: 1;
    grid-row-end: -1;
  }
  .sisr-image {
    position: relative;
    grid-column: 1 / 8;
    grid-row-start: 1;
    grid-row-end: -1;
  }
  .options-list {
    background-color: var(--dark-indigo);
    position: relative;
    padding: 15px 47px;

    z-index: 2;
    border-radius: 2px;
    font-family: var(--sfpro);
    color: var(--light-indigo2);
    font-weight: 400;
    font-size: 17px;
  }

  .bts-desc {
    margin-bottom: 111px;
  }
  .colored {
    color: var(--blue);
  }
  ul {
    margin: 0;
  }
  .overline {
    margin: 10px 0px;
    text-align: right;
    font-family: var(--ibm);
    color: var(--blue);
  }
  .option-title {
    text-align: right;
    font-family: var(--sfpro);
    color: var(--light-indigo);
    margin: 0px 0px 20px;
  }
  .sisr-tech-list {
    position: relative;
    display: flex;
    justify-content: flex-end;
    flex-wrap: wrap;
    gap: 17px;
    list-style: none;
    margin: 35px 0px 10px;
    padding: 0px;
    z-index: 2;
    font-family: var(--ibm);
    color: var(--light-indigo2);
    font-size: 15px;
  }
  .sisr-logo {
    display: flex;
    justify-content: flex-end;
    color: var(--light-indigo);
    gap: 10px;
  }
</style>
