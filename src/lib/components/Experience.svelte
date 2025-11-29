<script lang="ts">
  import SectionHeader from "./SectionHeader.svelte";

  const experienceItems = {
    Alstom: {
      title: "Stagiaire @",
      company: "Alstom",
      url: "https://www.alstom.com/fr",
      duration: "Mai 2025 - Juillet 2025",
      desc: [
        "Développé un script Python permettant la configuration automatique de switches HPE sur l’ensemble d’un projet ferroviaire.",
        "Réalisé des tests du script sur le matériel physique.",
        "Déployé et centralisé les outils d’automatisation existants dans Ansible.",
        "Manipulé des données Excel pour la génération automatique des fichiers de configuration.",
        "Étudié les besoins des ingénieurs réseaux afin d’adapter les solutions d’automatisation réseau.",
      ],
    },
    SAIGON: {
      title: "Stagiaire",
      company: "SAIGON",
      url: "",
      duration: "Novembre 2025 - Décembre 2025",
      desc: [""],
    },
  };
</script>

<section class="experience-section">
  <div class="section-header">
    <SectionHeader title={"/ Expérience"} />
  </div>
  <div class="experience">
    <div class="tabs">
      <button> Alstom</button>
      <button>SAIGON</button>
    </div>
    <div class="content">
      <h3></h3>
      <p></p>
      <ul>
        <li></li>
      </ul>
    </div>
  </div>
</section>
