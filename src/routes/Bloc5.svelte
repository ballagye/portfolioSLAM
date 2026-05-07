<script lang="ts">
  import Bloc from "../lib/components/Bloc.svelte";
  import ProjetAssocie from "../lib/components/ProjetAssocie.svelte";
  import { MoveUpRight } from "@lucide/svelte";

  let dialog16: HTMLDialogElement | undefined = undefined;
  function openDialog16() { dialog16?.showModal(); }
  function closeDialog16() { dialog16?.close(); }
  let dialog17: HTMLDialogElement | undefined = undefined;
  function openDialog17() { dialog17?.showModal(); }
  function closeDialog17() { dialog17?.close(); }
  let dialog18: HTMLDialogElement | undefined = undefined;
  function openDialog18() { dialog18?.showModal(); }
  function closeDialog18() { dialog18?.close(); }
</script>

<div class="bloc-title">
  <h2>/ Bloc 5 Mettre à disposition des utilisateurs un service informatique</h2>
</div>

<div class="competences-grid">
  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog16}
    onkeydown={(e) => e.key === "Enter" && openDialog16()}
  >
    <div class="valide">
      <h2 class="comp-title">C16</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Réaliser les tests d'intégration et d'acceptation d'un service</h3>
    <p>
      Tests du déploiement Prometheus et Grafana via Ansible Playbook en
      mode verbose…
    </p>
    <p class="rea-desc">Tests Ansible -- Projet personnel</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog17}
    onkeydown={(e) => e.key === "Enter" && openDialog17()}
  >
    <div class="valide">
      <h2 class="comp-title">C17</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Déployer un service informatique en environnement de production</h3>
    <p>
      Déploiement du script HPE, des playbooks Ansible (Prometheus & Grafana)
      et du portfolio sur Netlify…
    </p>
    <p class="rea-desc">Multi-projets — Stage Alstom & Personnel</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog18}
    onkeydown={(e) => e.key === "Enter" && openDialog18()}
  >
    <div class="valide">
      <h2 class="comp-title">C18</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Accompagner les utilisateurs dans la mise en place d'un service</h3>
    <p>
      Rédaction d'un guide d'utilisation du script HPE et suivi des ingénieurs
      réseau lors de l'adoption du projet…
    </p>
    <p class="rea-desc">Guide utilisateur — Stage Alstom</p>
  </div>
</div>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog16}
  onclick={(e) => e.target === dialog16 && closeDialog16()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog16}>✕</button>
    <Bloc
      competences="Compétence 16 - Réaliser les tests d'intégration et d'acceptation d'un service informatique"
      projectTitle="Tests du déploiement Prometheus et Grafana avec Ansible"
      date="2025"
      contexte="Réalisation:"
    />
    <p class="section-title">1. Déploiement Prometheus & Grafana</p>
    <ul class="tp-list">
      <li>Lancement des Playbooks Ansible en mode <code>--verbose</code> pour suivre chaque étape</li>
      <li>Identification et correction des erreurs de déploiement grâce aux logs</li>
      <li>Validation finale : Prometheus et Grafana opérationnels</li>
    </ul>

    <p class="section-title">2. Tests d'intégration — Hackathon</p>
    <ul class="tp-list">
      <li>Test de l'intégration des profils utilisateurs (nom, prénom, photo) dans la base de données</li>
      <li>Vérification du hachage des mots de passe côté front-end</li>
      <li>Validation du bon affichage et stockage des données</li>
    </ul>

    <p class="section-title">Bilan</p>
    <p>
      Dans les deux cas, les tests ont permis d'identifier des problèmes et de
      les corriger avant la mise en service finale.
    </p>
    <ProjetAssocie projets={[
      { nom: "Hackathon", contexte: "Formation · 2025" },
      { nom: "Déploiement Prometheus & Grafana", contexte: "Formation · 2025" }
    ]} />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <div class="proof-grid">
        <div class="proof-item">
          <img src="/Screenshot_10.png" alt="Tests Ansible Playbook verbose" />
          <p class="proof-caption">Ansible Playbook — Déploiement Prometheus & Grafana</p>
        </div>
        <div class="proof-item">
          <img src="/Screenshot_11.png" alt="Tests intégration hackathon" />
          <p class="proof-caption">Hackathon — Test profil développeur</p>
        </div>
        <div class="proof-item">
          <img src="/Screenshot_12.png" alt="Tests intégration hackathon 2" />
          <p class="proof-caption">Hackathon — Test profil développeur</p>
        </div>
      </div>
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog17}
  onclick={(e) => e.target === dialog17 && closeDialog17()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog17}>✕</button>
    <Bloc
      competences="Compétence 17 - Déployer un service informatique en environnement de production"
      projectTitle="Déploiement du script HPE, Ansible Playbooks et portfolio Netlify"
      date="2025"
      contexte="Réalisation:"
    />
    <p>
      Dans le cadre de plusieurs projets, j'ai eu l'occasion de déployer des
      services en environnement de production, chacun avec ses propres
      contraintes techniques.
    </p>
    <ul class="tp-list">
      <li>Déploiement du script d'automatisation HPE sur les projets ferroviaires (Turin, Cairo)</li>
      <li>Centralisation des outils d'automatisation existants de l'équipe dans Galaxie</li>
      <li>Écriture des playbooks Ansible pour le déploiement de Prometheus et Grafana</li>
      <li>Déploiement du portfolio sur Netlify avec CI/CD automatique depuis GitHub</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Chaque déploiement avait ses défis : configuration des serveurs pour les
      autorisations SSH des playbooks, compréhension de la syntaxe YAML et des
      modules Ansible. Le déploiement sur Netlify était simple grâce au CI/CD
      automatique depuis GitHub.
    </p>
    <ProjetAssocie projets={[
      { nom: "Déploiement portfolio", contexte: "Personnel · 2025" },
      { nom: "Déploiement GLPI", contexte: "Formation · 2025" },
      { nom: "Script d'automatisation HPE", contexte: "Stage Alstom · 2025" },
      { nom: "Déploiement Grafana et Prometheus avec Ansible", contexte: "Formation · 2025" }
    ]} />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <div class="proof-grid">
        <div class="proof-item">
          <video src="/graf-deployed.mp4" muted autoplay loop playsinline></video>
          <p class="proof-caption">Déploiement Grafana et Prometheus</p>
        </div>
        <div class="proof-item">
          <p class="proof-caption">Déploiement GLPI</p>
        </div>
      </div>
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog18}
  onclick={(e) => e.target === dialog18 && closeDialog18()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog18}>✕</button>
    <Bloc
      competences="Compétence 18 - Accompagner les utilisateurs dans la mise en place d'un service"
      projectTitle="Guide d'utilisation du script d'automatisation HPE — Stage Alstom"
      date="Mai - Juillet 2025"
      contexte="Réalisation:"
    />
    <p>
      Lors de mon stage chez Alstom, j'ai accompagné les ingénieurs réseau dans
      la prise en main du script d'automatisation que j'avais développé.
    </p>
    <ul class="tp-list">
      <li>Rédaction d'un guide d'utilisation complet : fonctionnement du script, projets concernés, étapes d'utilisation</li>
      <li>Présentation d'une vue d'ensemble du projet d'automatisation aux ingénieurs réseau</li>
      <li>Recueil des retours des ingénieurs sur l'outil et son utilisation</li>
      <li>Suivi de l'adoption du script par l'équipe réseau</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      La partie la plus exigeante a été de rédiger toute la documentation de A à
      Z, en rendant le projet compréhensible pour des utilisateurs qui n'avaient
      pas participé au développement. La documentation est confidentielle (projet
      interne Alstom).
    </p>
    <ProjetAssocie projets={[
      { nom: "Script d'automatisation HPE", contexte: "Stage Alstom · 2025" }
    ]} />
  </div>
</dialog>

<style>
  .bloc-title {
    display: flex;
    max-width: 1000px;
    margin: 0 auto;
  }
  h2 { font-family: var(--sfpro); }
  .competences-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 16px;
    max-width: 1000px;
    margin: 0 auto;
  }
  .competences {
    height: 270px;
    padding: 20px 24px;
    background-color: var(--dark-indigo);
    border-radius: 3px;
    cursor: pointer;
  }
  p { margin-top: 0; margin-bottom: 10px; font-family: var(--sfpro); }
  li { font-family: var(--sfpro); }
  .rea-title { font-family: var(--sfpro); font-size: 20px; margin-top: 0; margin-bottom: 10px; }
  .rea-desc { font-family: var(--ibm); color: var(--blue); }
  .comp-title { color: var(--blue); }
  .section-title { font-weight: 800; }
  .valide { display: flex; align-items: center; justify-content: space-between; }

  @keyframes dialog-in {
    from { opacity: 0; transform: translateY(16px) scale(0.97); }
    to   { opacity: 1; transform: translateY(0) scale(1); }
  }
  @keyframes backdrop-in {
    from { opacity: 0; } to { opacity: 1; }
  }
  dialog {
    background: var(--dark-indigo, #1a1a2e);
    border: 1px solid white;
    border-radius: 8px;
    padding: 0;
    max-width: 800px;
    width: 90vw;
    max-height: 90vh;
    overflow: hidden;
    color: inherit;
  }
  dialog[open] { animation: dialog-in 0.25s cubic-bezier(0.22, 1, 0.36, 1) both; }
  dialog::backdrop {
    background: rgba(0, 0, 0, 0.6);
    backdrop-filter: blur(2px);
    animation: backdrop-in 0.25s ease both;
  }
  .dialog-inner {
    padding: 24px;
    overflow-y: scroll;
    max-height: 90vh;
    position: relative;
    box-sizing: border-box;
  }
  .dialog-close {
    position: sticky;
    top: 0;
    float: right;
    background: none;
    border: none;
    color: inherit;
    font-size: 18px;
    cursor: pointer;
    opacity: 0.6;
    padding: 0 0 8px 8px;
  }
  .dialog-close:hover { opacity: 1; }
  .proof {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 24px;
  }
  .proof-label { font-family: var(--ibm); color: var(--blue); margin-bottom: 12px; }
  .proof-grid {
    display: flex;
    flex-direction: column;
    gap: 24px;
    width: 100%;
  }
  .proof-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
  }
  .proof-item img, .proof-item video { max-width: 100%; border-radius: 6px; }
  .proof-caption {
    font-family: var(--ibm);
    font-size: 11px;
    color: rgba(255, 255, 255, 0.5);
    text-align: center;
    margin: 0;
  }
</style>
