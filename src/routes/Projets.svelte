<script lang="ts">
  import { Github, Folder, ChevronDown } from "@lucide/svelte";
  import { Accordion } from "bits-ui";

  function blocUrl(comp: string): string {
    const num = parseInt(comp.match(/C(\d+)/)?.[1] ?? '0');
    if (num <= 6) return '/Bloc1';
    if (num <= 9) return '/Bloc2';
    if (num <= 12) return '/Bloc3';
    if (num <= 15) return '/Bloc4';
    if (num <= 18) return '/Bloc5';
    return '/Bloc6';
  }

  const projets = [
    {
      id: "devmate",
      titre: "DevMate",
      description: "Plateforme permettant la mise en relation entre des développeurs et des créateurs afin de réaliser des projets, qu'il s'agisse de sites web ou d'autres types de projets.",
      tech: ["Svelte", "TypeScript", "CSS"],
      github: "https://github.com/sudoPierre/DevMates/tree/DevMates-Svelte",
      competences: [
        "C14 — Planifier les activités d'un projet",
        "C15 — Évaluer les indicateurs de suivi et analyser les écarts",
        "C16 — Réaliser les tests d'intégration et d'acceptation",
      ],
    },
    {
      id: "ansible",
      titre: "Déploiement Prometheus & Grafana",
      description: "Automatisation du déploiement de Prometheus et Grafana via des playbooks Ansible.",
      tech: ["Ansible", "YAML", "Prometheus", "Grafana"],
      github: "https://github.com/ballagye/ansible-project",
      competences: [
        "C16 — Réaliser les tests d'intégration et d'acceptation",
        "C17 — Déployer un service informatique en production",
      ],
    },
    {
      id: "ecommerce",
      titre: "Site e-commerce",
      description: "Site web e-commerce de vente de produits avec panier et gestion des commandes.",
      tech: ["HTML", "CSS", "JavaScript"],
      github: "https://github.com/ballagye/Projet-dev",
      competences: [
        "C10 — Participer à la valorisation de l'image de l'organisation",
        "C12 — Participer à l'évolution d'un site Web",
        "C13 — Analyser les objectifs et les modalités d'organisation",
      ],
    },
    {
      id: "mbk",
      titre: "MBK Education",
      description: "Plateforme permettant d'exécuter du code pour résoudre des exercices.",
      tech: ["WordPress"],
      github: null,
      competences: [
        "C10 — Participer à la valorisation de l'image de l'organisation",
        "C11 — Référencer les services en ligne et mesurer leur visibilité",
        "C13 — Analyser les objectifs et les modalités d'organisation",
        "C14 — Planifier les activités d'un projet",
        "C16 — Réaliser les tests d'intégration et d'acceptation",
        "C17 — Déployer un service informatique en production",
      ],
    },
    {
      id: "login",
      titre: "Svelte Login",
      description: "Plateforme permettant de se connecter avec BetterAuth, utilisant plusieurs plateformes d'authentification notamment GitHub et d'autres services.",
      tech: ["Svelte", "BetterAuth", "TypeScript"],
      github: "https://github.com/ballagye/Svelte-Login",
      competences: [
        "C13 — Analyser les objectifs et les modalités d'organisation",
        "C14 — Planifier les activités d'un projet",
        "C16 — Réaliser les tests d'intégration et d'acceptation",
        "C17 — Déployer un service informatique en production",
      ],
    },
    {
      id: "chess",
      titre: "ChessGame",
      description: "Jeu d'échecs en langage C avec quelques règles spécifiques.",
      tech: ["C"],
      github: "https://github.com/ballagye/ChessGame",
      competences: [
        "C13 — Analyser les objectifs et les modalités d'organisation",
        "C14 — Planifier les activités d'un projet",
      ],
    },
  ];
</script>

<div class="section-header">
  <h2>/ Projets réalisés</h2>
</div>

<div class="projets-grid">
  {#each projets as projet}
    <div class="projet-card">

      <div class="card-top">
        <Folder size={40} class="folder-icon" />
        <div class="card-links">
          {#if projet.github}
            <a href={projet.github} target="_blank" class="icon-link">
              <Github size={20} />
            </a>
          {/if}
        </div>
      </div>

      <h3 class="projet-titre">{projet.titre}</h3>
      <p class="projet-desc">{projet.description}</p>

      <div class="card-footer">
        <div class="tech-row">
          {#each projet.tech as t}
            <span class="tech-tag">{t}</span>
          {/each}
        </div>

        <Accordion.Root type="single" class="accordion-root">
          <Accordion.Item value="comp">
            <Accordion.Trigger class="accordion-trigger">
              Voir les compétences
              <ChevronDown size={13} class="chevron-icon" />
            </Accordion.Trigger>
            <Accordion.Content class="accordion-content">
              <div class="comp-list">
                {#each projet.competences as c}
                  <a href={blocUrl(c)} class="comp-item">{c}</a>
                {/each}
              </div>
            </Accordion.Content>
          </Accordion.Item>
        </Accordion.Root>
      </div>

    </div>
  {/each}
</div>

<style>
  .section-header {
    max-width: 1000px;
    margin: 0 auto 8px;
  }
  h2 { font-family: var(--sfpro); }

  .projets-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 16px;
    max-width: 1000px;
    margin: 0 auto;
    align-items: start;
  }

  .projet-card {
    background-color: var(--dark-indigo);
    border-radius: 4px;
    padding: 26px;
    display: flex;
    flex-direction: column;
    gap: 12px;
    transition: transform 0.2s ease;
  }
  .projet-card:hover {
    transform: translateY(-5px);
  }

  .card-top {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  :global(.folder-icon) { color: var(--blue); }

  .card-links {
    display: flex;
    gap: 14px;
  }

  .icon-link {
    color: white;
    display: flex;
    align-items: center;
    transition: color 0.2s;
    text-decoration: none;
  }
  .icon-link:hover { color: white; }

  .projet-titre {
    font-family: var(--sfpro);
    font-size: 20px;
    font-weight: 700;
    color: white;
    margin: 6px 0 0;
  }

  .projet-desc {
    font-family: var(--sfpro);
    font-size: 14px;
    color: white;
    line-height: 1.6;
    margin: 0;
    flex: 1;
  }

  .card-footer {
    margin-top: auto;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }

  .tech-row {
    display: flex;
    flex-wrap: wrap;
    gap: 16px;
  }

  .tech-tag {
    font-family: var(--ibm);
    font-size: 12px;
    color: white;
  }

  :global(.accordion-root) { width: 100%; }

  :global(.accordion-trigger) {
    display: flex;
    align-items: center;
    gap: 5px;
    background: none;
    border: none;
    color: var(--blue);
    font-family: var(--ibm);
    font-size: 12px;
    cursor: pointer;
    padding: 0;
    transition: opacity 0.2s;
    width: 100%;
  }
  :global(.accordion-trigger:hover) { opacity: 0.7; }

  :global(.accordion-trigger[data-state="open"] .chevron-icon) {
    transform: rotate(180deg);
  }
  :global(.chevron-icon) { transition: transform 0.2s; }

  :global(.accordion-content[data-state="open"]) {
    animation: fadeIn 0.2s ease;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(-4px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .comp-list {
    display: flex;
    flex-direction: column;
    gap: 5px;
    margin-top: 10px;
    padding-top: 10px;
    border-top: 1px solid rgba(255, 255, 255, 0.07);
  }

  .comp-item {
    font-family: var(--sfpro);
    font-size: 12px;
    color: rgba(255, 255, 255, 0.6);
    padding: 5px 10px;
    background: rgba(255, 255, 255, 0.04);
    border-radius: 3px;
    text-decoration: none;
    transition: background 0.2s, color 0.2s;
  }
  .comp-item:hover {
    background: rgba(255, 255, 255, 0.1);
    color: white;
  }
</style>
