<script lang="ts">
  import Bloc from "../lib/components/Bloc.svelte";
  import ProjetAssocie from "../lib/components/ProjetAssocie.svelte";
  import { MoveUpRight } from "@lucide/svelte";

  let dialog13: HTMLDialogElement | undefined = undefined;
  function openDialog13() { dialog13?.showModal(); }
  function closeDialog13() { dialog13?.close(); }
  let dialog14: HTMLDialogElement | undefined = undefined;
  function openDialog14() { dialog14?.showModal(); }
  function closeDialog14() { dialog14?.close(); }
  let dialog15: HTMLDialogElement | undefined = undefined;
  function openDialog15() { dialog15?.showModal(); }
  function closeDialog15() { dialog15?.close(); }
</script>

<div class="bloc-title">
  <h2>/ Bloc 4 Travailler en mode projet</h2>
</div>

<div class="competences-grid">
  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog13}
    onkeydown={(e) => e.key === "Enter" && openDialog13()}
  >
    <div class="valide">
      <h2 class="comp-title">C13</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Analyser les objectifs et les modalités d'organisation d'un projet</h3>
    <p>
      Rédaction d'un cahier des charges et documentation complète du projet
      d'automatisation…
    </p>
    <p class="rea-desc">Documentation projet -- Stage Alstom</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog14}
    onkeydown={(e) => e.key === "Enter" && openDialog14()}
  >
    <div class="valide">
      <h2 class="comp-title">C14</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Planifier les activités d'un projet</h3>
    <p>
      Utilisation de Trello avec la méthode Kanban lors d'un hackathon en
      groupe de 3…
    </p>
    <p class="rea-desc">Trello Kanban -- Hackathon</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog15}
    onkeydown={(e) => e.key === "Enter" && openDialog15()}
  >
    <div class="valide">
      <h2 class="comp-title">C15</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Évaluer les indicateurs de suivi d'un projet et analyser les écarts</h3>
    <p>
      Bilan du hackathon : suivi des fonctionnalités, identification des écarts
      et priorisation…
    </p>
    <p class="rea-desc">Bilan projet -- Hackathon</p>
  </div>
</div>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog13}
  onclick={(e) => e.target === dialog13 && closeDialog13()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog13}>✕</button>
    <Bloc
      competences="Compétence 13 - Analyser les objectifs et les modalités d'organisation d'un projet"
      projectTitle="Documentation et cahier des charges du projet d'automatisation des switchs HPE"
      date="Mai - Juillet 2025"
      contexte="Réalisation:"
    />
    <p>
      Lors de mon stage de première année chez Alstom, j'ai rédigé la
      documentation complète du projet d'automatisation, depuis l'étude des
      besoins jusqu'à la conception technique du script.
    </p>
    <ul class="tp-list">
      <li>Étude des besoins des ingénieurs réseau sur les projets ferroviaires</li>
      <li>Rédaction d'un cahier des charges définissant les objectifs et le périmètre du projet</li>
      <li>Documentation du flux complet : import des données Excel depuis NetArt → génération des fichiers <code>.cfg</code> → connexion SSH aux switchs</li>
      <li>Création de schémas illustrant l'architecture et les étapes du projet</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Cette documentation a cadré toutes les étapes de réalisation et a servi
      de référence tout au long du développement du script.
    </p>
    <ProjetAssocie projets={[{ nom: "Développement script Python HPE", contexte: "Stage Alstom · 2025" }]} />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img src="/Screenshot_8.png" alt="Documentation projet automatisation" />
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog14}
  onclick={(e) => e.target === dialog14 && closeDialog14()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog14}>✕</button>
    <Bloc
      competences="Compétence 14 - Planifier les activités d'un projet en utilisant des méthodes agiles et des outils de suivi"
      projectTitle="Organisation d'un hackathon avec Trello et la méthode Kanban"
      date="2025"
      contexte="Réalisation:"
    />
    <p>
      Dans le cadre d'un hackathon en groupe de 3, j'ai utilisé Trello avec la
      méthode Kanban pour planifier et organiser les tâches du projet.
    </p>
    <ul class="tp-list">
      <li>Création d'un tableau Trello avec les colonnes À faire, En cours, Terminé</li>
      <li>Répartition des tâches entre les 3 membres de l'équipe</li>
      <li>Suivi de l'avancement en temps réel via le tableau Kanban</li>
      <li>Coordination et communication entre les membres tout au long du projet</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      L'utilisation de Trello et du Kanban a permis de maintenir une vision
      claire de l'avancement et d'assurer une bonne répartition du travail au
      sein de l'équipe.
    </p>
    <ProjetAssocie projets={[{ nom: "Hackathon", contexte: "Formation · 2025" }]} />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <div class="proof-grid">
        <div class="proof-item">
          <img src="/Screenshot_9.png" alt="Trello Kanban hackathon" />
          <p class="proof-caption">Hackathon — Tableau Kanban</p>
        </div>
        <div class="proof-item">
          <img src="/screenshotchess.png" alt="ChessGame C" />
        </div>
        <div class="proof-item">
          <img src="/mbkeducationgantt.png" alt="MBK Education Gantt" />
          <p class="proof-caption">MBK Education — Planification des activités via un diagramme de Gantt</p>
        </div>
      </div>
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog15}
  onclick={(e) => e.target === dialog15 && closeDialog15()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog15}>✕</button>
    <Bloc
      competences="Compétence 15 - Évaluer les indicateurs de suivi d'un projet et analyser les écarts"
      projectTitle="Bilan et analyse des écarts lors d'un hackathon"
      date="2025"
      contexte="Réalisation:"
    />
    <p>
      À l'issue du hackathon, j'ai participé à un bilan du projet permettant
      d'évaluer l'avancement réel par rapport aux objectifs initiaux.
    </p>
    <ul class="tp-list">
      <li>Suivi des fonctionnalités du site réalisées pendant le hackathon</li>
      <li>Identification des fonctionnalités non terminées et analyse des causes (manque de temps)</li>
      <li>Priorisation des fonctionnalités essentielles au bon fonctionnement du projet</li>
      <li>Définition des axes d'amélioration pour une version future</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Le projet était fonctionnel à la fin du hackathon, mais non finalisé :
      certaines fonctionnalités n'ont pas pu être implémentées faute de temps.
      Ce bilan a permis d'identifier clairement les écarts entre les objectifs
      fixés et le réalisé.
    </p>
    <ProjetAssocie projets={[{ nom: "Hackathon", contexte: "Formation · 2025" }]} />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img src="/Screenshot_9.png" alt="Bilan hackathon" />
    </div>
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
  .proof img { max-width: 100%; border-radius: 6px; }
  .proof-grid { display: flex; flex-direction: column; gap: 24px; width: 100%; }
  .proof-item { display: flex; flex-direction: column; align-items: center; gap: 8px; }
  .proof-item img { max-width: 100%; border-radius: 6px; }
  .proof-caption { font-family: var(--ibm); font-size: 11px; color: rgba(255,255,255,0.5); text-align: center; margin: 0; }
</style>
