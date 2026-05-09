<script lang="ts">
  import Bloc from "../lib/components/Bloc.svelte";
  import ProjetAssocie from "../lib/components/ProjetAssocie.svelte";
  import { MoveUpRight } from "@lucide/svelte";

  let dialog10: HTMLDialogElement | undefined = undefined;
  function openDialog10() {
    dialog10?.showModal();
  }
  function closeDialog10() {
    dialog10?.close();
  }
  let dialog11: HTMLDialogElement | undefined = undefined;
  function openDialog11() {
    dialog11?.showModal();
  }
  function closeDialog11() {
    dialog11?.close();
  }
  let dialog12: HTMLDialogElement | undefined = undefined;
  function openDialog12() {
    dialog12?.showModal();
  }
  function closeDialog12() {
    dialog12?.close();
  }
</script>

<div class="bloc-title">
  <h2>/ Bloc 3 Développer la présence en ligne de l'organisation</h2>
</div>

<div class="competences-grid">
  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog10}
    onkeydown={(e) => e.key === "Enter" && openDialog10()}
  >
    <div class="valide">
      <h2 class="comp-title">C10</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">
      Participer à la valorisation de l'image de l'organisation sur les médias
      numériques
    </h3>
    <p>
      Création d'un profil LinkedIn complet et développement d'un réseau
      professionnel…
    </p>
    <p class="rea-desc">LinkedIn -- Développement professionnel</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog11}
    onkeydown={(e) => e.key === "Enter" && openDialog11()}
  >
    <div class="valide">
      <h2 class="comp-title">C11</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">
      Référencer les services en ligne et mesurer leur visibilité
    </h3>
    <p>
      Optimisation SEO d'un site web — attributs alt, descriptions et bonnes
      pratiques…
    </p>
    <p class="rea-desc">SEO -- Formation</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog12}
    onkeydown={(e) => e.key === "Enter" && openDialog12()}
  >
    <div class="valide">
      <h2 class="comp-title">C12</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Participer à l'évolution d'un site web</h3>
    <p>Refonte d'un site existant, merge GitHub et déploiement Netlify…</p>
    <p class="rea-desc">Refonte site vitrine -- Stage 2</p>
  </div>
</div>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog10}
  onclick={(e) => e.target === dialog10 && closeDialog10()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog10}>✕</button>
    <Bloc
      competences="Compétence 10 - Participer à la valorisation de l'image de l'organisation sur les médias numériques"
      projectTitle="Création et développement d'un profil LinkedIn professionnel"
      date="Septembre 2024"
      contexte="Réalisation:"
    />
    <p>
      J'ai créé un profil LinkedIn complet en partant de zéro pour développer ma
      présence professionnelle en ligne.
    </p>
    <ul class="tp-list">
      <li>
        Rédaction d'un résumé mettant en avant ma formation BTS SIO et mes
        stages
      </li>
      <li>Ajout des expériences, compétences et formations</li>
      <li>
        Prise de contact avec des professionnels du secteur IT pour développer
        mon réseau
      </li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Cette démarche m'a permis de construire une présence numérique
      professionnelle et de constituer un premier réseau de contacts dans le
      secteur informatique.
    </p>
    <ProjetAssocie
      projets={[
        {
          nom: "Création profils LinkedIn & GitHub",
          contexte: "Personnel · 2024",
        },
      ]}
    />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img src="/Screenshot_5.png" alt="Profil LinkedIn" />
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog11}
  onclick={(e) => e.target === dialog11 && closeDialog11()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog11}>✕</button>
    <Bloc
      competences="Compétence 11 - Référencer les services en ligne de l'organisation et mesurer leur visibilité"
      projectTitle="Optimisation SEO de mon portfolio"
      date="Novembre - Décembre 2025"
      contexte="Réalisation:"
    />
    <p>
      J'ai appliqué les bonnes pratiques SEO sur mon portfolio pour améliorer sa
      visibilité auprès des moteurs de recherche.
    </p>
    <ul class="tp-list">
      <li>
        Ajout d'attributs <code>alt</code> descriptifs sur toutes les images
      </li>
      <li>
        Vérification de la hiérarchie des balises <code>h1</code>,
        <code>h2</code>…
      </li>
      <li>Rédaction de descriptions avec des mots-clés pertinents</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Ces optimisations permettent aux moteurs de recherche de mieux indexer le
      contenu et améliorent l'accessibilité du portfolio.
    </p>
    <ProjetAssocie
      projets={[
        { nom: "Réalisation du portfolio", contexte: "Formation · 2025" },
      ]}
    />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img src="/Screenshot_6.png" alt="SEO site vitrine" />
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog12}
  onclick={(e) => e.target === dialog12 && closeDialog12()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog12}>✕</button>
    <Bloc
      competences="Compétence 12 - Participer à l'évolution d'un site web exploitant les données de l'organisation"
      projectTitle="Refonte d'un site vitrine existant avec déploiement sur Netlify"
      date="Novembre - Décembre 2025"
      contexte="Réalisation:"
    />
    <p>
      Lors de mon deuxième stage, j'ai participé à la refonte d'un site vitrine
      existant en travaillant en équipe via GitHub, avec déploiement automatique
      sur Netlify.
    </p>
    <ul class="tp-list">
      <li>
        Intégration dans le repository partagé et commits réguliers sur une
        branche dédiée
      </li>
      <li>Merge final sur la branche principale en fin de stage</li>
      <li>
        Amélioration de l'identité visuelle dans le respect de la charte
        existante
      </li>
      <li>
        CI Netlify : chaque merge déclenche automatiquement une mise à jour du
        site
      </li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Le site a été livré et déployé automatiquement, avec un historique de
      modifications accessible à toute l'équipe.
    </p>
    <ProjetAssocie
      projets={[
        { nom: "Refonte site vitrine Svelte", contexte: "Stage 2 · 2025" },
      ]}
    />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img src="/Screenshot_7.png" alt="Déploiement Netlify CI" />
    </div>
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
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
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

  .proof img { max-width: 100%; border-radius: 6px; }
</style>
