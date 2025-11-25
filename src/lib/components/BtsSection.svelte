<script>
  import SectionHeader from "./SectionHeader.svelte";
  import Images from "./Images.svelte";
</script>

<section id="bts-sio">
  <div class="section-header"><SectionHeader /></div>
  <div class="bts-desc">
    <p>
      Le Brevet de Technicien Supérieur aux Services Informatiques aux
      Organisations (BTS SIO) est un <br />programme de niveau Bac+2 et
      s’adresse aux personnes qui souhaitent se former en deux ans aux métiers
      d’administrateurs réseau ou de développeur
    </p>
    <br />
    <p>
      Il peut-être réalisable soit en alternance d’une durée de 12 ou de 24 ou
      alors en initial avec un minimum de <br />10 semaines de stages
      obligatoire en entreprise d’une durée de 2 à 3 mois, afin de s’initier aux
      réalités du domaine professionnel.
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
          <div class="sisr-description">
            <ul class="sisr-text">
              <li>
                Gestion des systèmes d’exploitation et des services réseaux
              </li>
              <li>Gestion et la maintenance des infrastructures réseau</li>
              <li>Optimisation des performances d’un réseau</li>
              <li>Sécurisations des infrastructures</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="sisr-image"><Images /></div>
    </li>

    <div>
      <ul class="sisr-tech-list">
        <li>Machines Virtuelles</li>
        <li>Linux</li>
        <li>Debian</li>
        <li>Ubuntu</li>
        <li>Windows Server</li>
      </ul>
    </div>
  </ul>
</section>

<style>
  .bts-desc {
    display: flex;
    flex-direction: column;
    margin: 0px;
  }

  p {
    margin: 0px 25px 0px 25px;
    font-family: "SF Pro Display", sans-serif;
    color: oklch(96.2% 0.018 272.314);
    font-family: "SF Pro Display", sans-serif;
    font-size: 24px;
  }
  .sisr-description {
    box-shadow: 0 10px 30px -15px var(--navy-shadow);
    transition: var(--transition);
    position: relative;
    z-index: 2;
    padding: 25px;
    border-radius: var(--border-radius);
    background-color: var(--indigo-dark);
  }
  .sisr-content {
    grid-area: 1 / 2 / -1 / 8;
    position: relative;
    text-align: right;
  }
  .sisr-text {
    display: inline-block;

    font-family: "SF Pro Display", sans-serif;
    color: var(--light-indigo);
  }
  .sisr-overline {
    font-family: "IBM Plex Mono";
    color: var(--blue);
    margin-right: 0px;
    padding: 0;
  }
  .sisr-title {
    font-family: "SF Pro Display", sans-serif;
    color: white;
  }
  #bts-sio {
    margin: 0px 202px;
    padding: 100px 0px;
  }
  .sisr-section {
    list-style-type: none;
    position: relative;
    display: grid;

    align-items: center;
  }
  .sisr-image {
    box-shadow: 0 10px 30px -15px var(--navy-shadow);
    transition: var(--transition);
    grid-area: 1 / 6 / -1 / -1;
    position: relative;
    z-index: 2;
  }
  .sisr-tech-list {
    display: flex;
    gap: 10px;
    position: relative;
    margin: 27px 0px 10px;
    padding: 0px;
    justify-content: flex-end;
    list-style: none;
    font-family: "IBM Plex mono";
    color: var(--light-indigo);
  }
</style>
