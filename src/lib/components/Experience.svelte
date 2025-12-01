<script lang="ts">
  import SectionHeader from "./SectionHeader.svelte";
  import { Tabs } from "bits-ui";
  import { fade } from "svelte/transition";
</script>

<section class="experience-section">
  <div class="section-header">
    <SectionHeader title={"/ Expérience"} />
  </div>
  <div class="tabs">
    <Tabs.Root
      value="alstom"
      data-tabs-root
      style="display: flex;
      align-items: baseline;
      gap: 50px;
      "
    >
      <Tabs.List
        style="display: grid;
      "
      >
        <Tabs.Trigger value="alstom">
          {#snippet child({ props })}
            <button {...props} class="scoped-button"> Alstom</button>
          {/snippet}

          Alstom</Tabs.Trigger
        >
        <Tabs.Trigger value="saigon">
          {#snippet child({ props })}
            <button {...props} class="scoped-button"> SAIGON</button>
          {/snippet}

          Saigon</Tabs.Trigger
        >
      </Tabs.List>
      <Tabs.Content value="alstom">
        <div class="alstom-content tab-content">
          <h3>
            <span>Stage DevOps (Python, Ansible)</span>
            <span class="at"> @ </span>
            <a href="https://www.alstom.com/fr" target="_blank" class="company">
              Alstom</a
            >
          </h3>
          <p>Mai 2025 - Juillet 2025</p>
          <ul>
            <li>
              Développé un script Python permettant la configuration automatique
              de switches HPE sur l’ensemble du projet ferroviaire.
            </li>
            <li>
              Manipulation des données Excel afin de générer les fichiers de
              configuration nécessaires.
            </li>
            <li>
              Réalisation de tests du script directement sur le matériel
              physique pour valider son fonctionnement.
            </li>
            <li>
              Déployé et centralisé les outils d’automatisation existants dans
              Ansible.
            </li>
            <li>
              Étude des besoins des ingénieurs réseaux pour adapter les
              solutions d’automatisation.
            </li>
          </ul>
        </div>
      </Tabs.Content>
      <Tabs.Content value="saigon">
        <div class="saigon-content tab-content">
          <h3>
            <span>Stage</span>
            <span class="at"> @ </span>
            <a href="" target="_blank" class="company"> SAIGON</a>
          </h3>
          <p>Novembre 2025 - Décembre 2025</p>
          <ul>
            <li>
              Modernisation des outils internes de en migrant le système de
              gestion de stock et de comptabilité d’Excel vers une application
              Java.
            </li>
            <li>
              Conception de l’architecture de la nouvelle application Java.
            </li>
            <li>
              Amélioration du front-end du site web et création de systèmes de
              commandes client.
            </li>
            <li>
              Développement d’un tableau de bord permettant au personnel de
              visualiser les commandes.
            </li>

            <li>
              Création et configuration de la base de données liée à
              l’application depuis l’export Excel.
            </li>
          </ul>
        </div>
      </Tabs.Content>
    </Tabs.Root>
  </div>
</section>

<style>
  .experience-section {
    margin: 0px auto;
    max-width: 1100px;
  }
  h3 {
    font-family: var(--sfpro);
    color: var(--light-indigo);
    margin-bottom: 8px;
    font-size: 20px;
  }
  .company {
    position: relative;
    text-decoration: none;
    color: var(--blue);
  }
  .company:hover {
    scale: 1.2;
    text-decoration: underline;
    text-decoration-thickness: 1px;
    text-underline-offset: 4px;
  }
  .at {
    text-decoration: none;
    color: var(--blue);
  }
  p {
    font-family: var(--ibm);
    color: var(--light-indigo2);
    font-size: 14px;
    margin-bottom: 25px;
    margin: 0px;
  }
  .scoped-button {
    background-color: transparent;
    background-repeat: no-repeat;
    border: none;
    cursor: pointer;
    overflow: hidden;
    outline: none;
    font-size: var(--fz-xs);
    font-family: var(--ibm);
    color: var(--light-indigo2);
    padding: 0px 20px 2px;
    border-right: 2px solid;
    height: var(--tab-height);
    transition-duration: 300ms;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-delay: 0ms;
    transition-property: all;
  }

  [data-tabs-trigger][data-state="active"] {
    color: var(--blue);
  }

  [data-tabs-content][data-state="active"].alstom-content {
    opacity: 1;
    transform: translateY(0);
  }
  .tab-content {
    animation: fade-up 0.5s ease-out;
  }

  ul {
    font-family: var(--sfpro);
    color: var(--light-indigo2);
    list-style: none;
    max-width: 600px;
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

  @keyframes fade-up {
    0% {
      opacity: 0.2;
      transform: translateY(15px) scale(1);
    }
  }
</style>
