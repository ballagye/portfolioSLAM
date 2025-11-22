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
</style>
