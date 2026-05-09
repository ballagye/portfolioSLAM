<script lang="ts">
  import Bloc from "../lib/components/Bloc.svelte";
  import ProjetAssocie from "../lib/components/ProjetAssocie.svelte";
  import { MoveUpRight } from "@lucide/svelte";

  let dialog7: HTMLDialogElement | undefined = undefined;
  function openDialog7() { dialog7?.showModal(); }
  function closeDialog7() { dialog7?.close(); }
  let dialog8: HTMLDialogElement | undefined = undefined;
  function openDialog8() { dialog8?.showModal(); }
  function closeDialog8() { dialog8?.close(); }
  let dialog9: HTMLDialogElement | undefined = undefined;
  function openDialog9() { dialog9?.showModal(); }
  function closeDialog9() { dialog9?.close(); }
</script>

<div class="bloc-title">
  <h2>/ Bloc 2 Répondre aux incidents et aux demandes d'assistance et d'évolution</h2>
</div>

<div class="competences-grid">
  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog7}
    onkeydown={(e) => e.key === "Enter" && openDialog7()}
  >
    <div class="valide">
      <h2 class="comp-title">C7</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Collecter, suivre et orienter des demandes</h3>
    <p>
      Paramétrage de GLPI avec catégories, priorités et attribution des
      tickets…
    </p>
    <p class="rea-desc">Gestion des tickets GLPI -- Formation</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog8}
    onkeydown={(e) => e.key === "Enter" && openDialog8()}
  >
    <div class="valide">
      <h2 class="comp-title">C8</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Traiter les demandes concernant les services réseau et système</h3>
    <p>
      Consultation des documentations HPE et NOKIA, diagnostic et résolution
      des incidents SSH…
    </p>
    <p class="rea-desc">Configuration switchs -- Alstom</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog9}
    onkeydown={(e) => e.key === "Enter" && openDialog9()}
  >
    <div class="valide">
      <h2 class="comp-title">C9</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Traiter les demandes concernant les applications</h3>
    <p>
      Refactorisation du logiciel d'automatisation suite aux retours du
      tuteur…
    </p>
    <p class="rea-desc">Classe SSHManager -- Alstom</p>
  </div>
</div>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog7}
  onclick={(e) => e.target === dialog7 && closeDialog7()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog7}>✕</button>
    <Bloc
      competences="Compétence 7 - Collecter, suivre et orienter des demandes"
      projectTitle="Paramétrage du système de ticketing GLPI"
      date="Octobre 2025"
      contexte="Réalisation:"
    />
    <p>
      Dans le cadre d'un TP sur GLPI, j'ai paramétré un système de ticketing
      pour gérer les demandes d'une organisation fictive.
    </p>
    <ul class="tp-list">
      <li>Création de 6 catégories : Réseau, Matériel, Logiciel, Sécurité, Messagerie, Autre</li>
      <li>Configuration des niveaux de priorité (Très haute, Haute, Moyenne, Basse) selon la matrice ITIL</li>
      <li>Mise en place de règles d'attribution automatique vers le technicien compétent</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      J'ai catégorisé plusieurs tickets afin de mettre en place un service
      informatique proche des pratiques en entreprise. Cette organisation facilite
      la résolution des demandes en orientant chaque ticket vers la bonne
      catégorie et le bon technicien, réduisant ainsi les délais de traitement.
    </p>
    <ProjetAssocie projets={[{ nom: "Paramétrage du système de ticketing GLPI", contexte: "Formation · Oct 2025" }]} />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img src="/Screenshot_4.png" alt="Tickets GLPI paramétrés" />
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog8}
  onclick={(e) => e.target === dialog8 && closeDialog8()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog8}>✕</button>
    <Bloc
      competences="Compétence 8 - Traiter les demandes concernant les services réseau et système, diagnostiquer les incidents"
      projectTitle="Configuration des switchs HPE et NOKIA et résolution des incidents SSH"
      date="Mai - Juillet 2025"
      contexte="Réalisation:"
    />
    <p>
      Durant mon stage chez Alstom, j'ai configuré des switchs HPE et NOKIA
      en consultant leurs documentations, et résolu des problèmes de connexion SSH.
    </p>
    <ul class="tp-list">
      <li>Lecture des documentations HPE et NOKIA pour adapter les fichiers de configuration à chaque matériel</li>
      <li>Diagnostic des connexions SSH qui ne fonctionnaient pas initialement</li>
      <li>Correction des paramètres et validation des connexions via Netmiko</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Les connexions SSH ont été rétablies, permettant la reprise des tests
      automatisés sur les équipements.
    </p>
    <ProjetAssocie projets={[
      { nom: "Développement script Python HPE", contexte: "Stage Alstom · 2025" },
      { nom: "Tests SSH avec Netmiko", contexte: "Stage Alstom · 2025" }
    ]} />
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog9}
  onclick={(e) => e.target === dialog9 && closeDialog9()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog9}>✕</button>
    <Bloc
      competences="Compétence 9 - Traiter les demandes concernant les applications"
      projectTitle="Refactorisation du logiciel d'automatisation — création de la classe SSHManager"
      date="Mai - Juillet 2025"
      contexte="Réalisation:"
    />
    <p>
      Suite aux retours de mon tuteur, j'ai restructuré le code de mon logiciel
      en créant une classe dédiée à la gestion des connexions SSH.
    </p>
    <ul class="tp-list">
      <li>Problème identifié : la logique SSH était mélangée à d'autres classes, rendant le code difficile à maintenir</li>
      <li>Création de la classe <code>SSHManager</code> regroupant toute la gestion des connexions</li>
      <li>Les autres classes délèguent désormais entièrement à <code>SSHManager</code></li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Mon code initial présentait plusieurs problèmes de lisibilité et de
      compréhension. J'ai entrepris une refactorisation complète afin de le
      structurer de manière claire et modulaire, permettant à tout développeur
      de le comprendre et de faire évoluer le projet plus facilement à l'avenir.
    </p>
    <ProjetAssocie projets={[{ nom: "Développement script Python HPE", contexte: "Stage Alstom · 2025" }]} />
  </div>
</dialog>

<style>
  .bloc-title {
    display: flex;
    max-width: 1000px;
    margin: 0 auto;
  }

  h2 {
    font-family: var(--sfpro);
  }

  .competences-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 16px;
    max-width: 1000px;
    margin: 0 auto;
  }

  .competences {
    height: 270px;
    padding: 20px 24px 20px 24px;
    background-color: var(--dark-indigo);
    border-radius: 3px;
    cursor: pointer;
  }

  p {
    margin-top: 0px;
    margin-bottom: 10px;
    font-family: var(--sfpro);
  }
  li {
    font-family: var(--sfpro);
  }
  .rea-title {
    font-family: var(--sfpro);
    font-size: 20px;
    margin-top: 0px;
    margin-bottom: 10px;
  }
  .rea-desc {
    font-family: var(--ibm);
    color: var(--blue);
  }
  .comp-title {
    color: var(--blue);
  }
  .section-title {
    font-weight: 800;
  }
  .valide {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  @keyframes dialog-in {
    from {
      opacity: 0;
      transform: translateY(16px) scale(0.97);
    }
    to {
      opacity: 1;
      transform: translateY(0) scale(1);
    }
  }

  @keyframes backdrop-in {
    from { opacity: 0; }
    to   { opacity: 1; }
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

  dialog[open] {
    animation: dialog-in 0.25s cubic-bezier(0.22, 1, 0.36, 1) both;
  }

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

  .dialog-close:hover {
    opacity: 1;
  }

  .proof {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 24px;
  }

  .proof-label {
    font-family: var(--ibm);
    color: var(--blue);
    margin-bottom: 12px;
  }

  .proof img {
    max-width: 100%;
    border-radius: 6px;
  }
</style>
