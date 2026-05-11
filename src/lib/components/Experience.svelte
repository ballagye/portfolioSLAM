<script lang="ts">
  import SectionHeader from "./SectionHeader.svelte";
  import { Tabs, Accordion } from "bits-ui";
  import { ChevronDown } from "@lucide/svelte";

  function navTo(href: string) {
    window.history.pushState({}, "", href);
    window.dispatchEvent(new PopStateEvent("popstate"));
  }

  const compAlstom = [
    {
      tags: ["C4", "C5"],
      href: "/Bloc1",
      desc: "Sauvegardes des configurations switches sur SharePoint et continuité du service réseau.",
    },
    {
      tags: ["C8", "C9"],
      href: "/Bloc2",
      desc: "Diagnostic et résolution des connexions SSH, refactorisation du script SSHManager.",
    },
    {
      tags: ["C13", "C14"],
      href: "/Bloc4",
      desc: "Cahier des charges du projet d'automatisation et planification des étapes.",
    },
    {
      tags: ["C16", "C17", "C18"],
      href: "/Bloc5",
      desc: "Tests Ansible verbose, déploiement sur projets ferroviaires, guide utilisateur pour les ingénieurs réseau.",
    },
  ];

  const compSaigon = [
    {
      tags: ["C6"],
      href: "/Bloc1",
      desc: "Correction des polices libres de droit signalée par le tuteur, intégrée avant publication.",
    },
    {
      tags: ["C9", "C13"],
      href: "/Bloc2",
      desc: "Développement de l'application Java et conception de l'architecture du projet.",
    },
    {
      tags: ["C10", "C12"],
      href: "/Bloc3",
      desc: "Amélioration du front-end et évolution du site web de l'organisation.",
    },
  ];
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
              Modélisation et intégration d’un environnement CI/CD au sein du
              département Network & IT, contribuant à l’automatisation des
              tâches manuelles.
            </li>

            <li>
              Conception et développement d’un script Python permettant la
              configuration automatique de switchs HPE sur l’ensemble d’un
              projet ferroviaire, réduisant ainsi le temps des déploiements.
            </li>
            <li>
              Manipulation et extraction de données Excel pour la génération de
              fichiers de configuration.
            </li>
            <li>Réalisation de tests du script sur le matériel physique.</li>
            <li>
              Déployé et centralisé les outils d'automatisation existants dans
              Ansible.
            </li>
            <li>
              Étude des besoins des ingénieurs réseaux afin d’adapter les
              solutions d’automatisation réseau.
            </li>
          </ul>
          <Accordion.Root type="single" class="acc-root">
            <Accordion.Item value="comp">
              <Accordion.Trigger class="acc-trigger">
                Voir les compétences <ChevronDown
                  size={13}
                  class="acc-chevron"
                />
              </Accordion.Trigger>
              <Accordion.Content class="acc-content">
                <div class="comp-list">
                  {#each compAlstom as g}
                    <a
                      href={g.href}
                      class="comp-item"
                      onclick={(e) => {
                        e.preventDefault();
                        navTo(g.href);
                      }}
                    >
                      <span class="comp-tags">
                        {#each g.tags as t}<span class="comp-tag">{t}</span
                          >{/each}
                      </span>
                      <span class="comp-desc">{g.desc}</span>
                    </a>
                  {/each}
                </div>
              </Accordion.Content>
            </Accordion.Item>
          </Accordion.Root>
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
              gestion de stock d'Excel vers une application Java.
            </li>
            <li>
              Refonte du front-end du site web vitrine en Svelte modernisant
              l'éxperience utilisateur
            </li>
            <li>Etude des ajouts possible sur le site web de l'entreprise</li>
          </ul>
          <Accordion.Root type="single" class="acc-root">
            <Accordion.Item value="comp">
              <Accordion.Trigger class="acc-trigger">
                Voir les compétences <ChevronDown
                  size={13}
                  class="acc-chevron"
                />
              </Accordion.Trigger>
              <Accordion.Content class="acc-content">
                <div class="comp-list">
                  {#each compSaigon as g}
                    <a
                      href={g.href}
                      class="comp-item"
                      onclick={(e) => {
                        e.preventDefault();
                        navTo(g.href);
                      }}
                    >
                      <span class="comp-tags">
                        {#each g.tags as t}<span class="comp-tag">{t}</span
                          >{/each}
                      </span>
                      <span class="comp-desc">{g.desc}</span>
                    </a>
                  {/each}
                </div>
              </Accordion.Content>
            </Accordion.Item>
          </Accordion.Root>
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

  :global(.acc-root) {
    margin-top: 20px;
    max-width: 600px;
  }

  :global(.acc-trigger) {
    display: flex;
    align-items: center;
    gap: 6px;
    background: none;
    border: none;
    color: var(--blue);
    font-family: var(--ibm);
    font-size: 13px;
    cursor: pointer;
    padding: 0;
    transition: opacity 0.2s;
  }
  :global(.acc-trigger:hover) {
    opacity: 0.7;
  }
  :global(.acc-trigger[data-state="open"] .acc-chevron) {
    transform: rotate(180deg);
  }
  :global(.acc-chevron) {
    transition: transform 0.2s;
  }

  .comp-list {
    display: flex;
    flex-direction: column;
    gap: 5px;
    margin-top: 10px;
  }
  .comp-item {
    display: flex;
    align-items: baseline;
    gap: 12px;
    padding: 8px 12px;
    background: rgba(255, 255, 255, 0.04);
    border-radius: 3px;
    text-decoration: none;
    transition: background 0.2s;
  }
  .comp-item:hover {
    background: rgba(255, 255, 255, 0.08);
  }

  .comp-tags {
    display: flex;
    gap: 5px;
    flex-shrink: 0;
  }
  .comp-tag {
    font-family: var(--ibm);
    font-size: 11px;
    font-weight: 700;
    color: var(--blue);
    border: 1px solid var(--blue);
    border-radius: 3px;
    padding: 1px 6px;
    white-space: nowrap;
  }
  .comp-desc {
    font-family: var(--sfpro);
    font-size: 13px;
    color: var(--light-indigo2);
    line-height: 1.4;
  }

  @keyframes fade-up {
    0% {
      opacity: 0.2;
      transform: translateY(15px) scale(1);
    }
  }
</style>
