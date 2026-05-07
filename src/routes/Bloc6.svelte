<script lang="ts">
  import Bloc from "../lib/components/Bloc.svelte";
  import ProjetAssocie from "../lib/components/ProjetAssocie.svelte";
  import { MoveUpRight } from "@lucide/svelte";

  let dialog19: HTMLDialogElement | undefined = undefined;
  function openDialog19() { dialog19?.showModal(); }
  function closeDialog19() { dialog19?.close(); }
  let dialog20: HTMLDialogElement | undefined = undefined;
  function openDialog20() { dialog20?.showModal(); }
  function closeDialog20() { dialog20?.close(); }
  let dialog21: HTMLDialogElement | undefined = undefined;
  function openDialog21() { dialog21?.showModal(); }
  function closeDialog21() { dialog21?.close(); }
  let dialog22: HTMLDialogElement | undefined = undefined;
  function openDialog22() { dialog22?.showModal(); }
  function closeDialog22() { dialog22?.close(); }
</script>

<div class="bloc-title">
  <h2>/ Bloc 6 Organiser son développement professionnel</h2>
</div>

<div class="competences-grid">
  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog19}
    onkeydown={(e) => e.key === "Enter" && openDialog19()}
  >
    <div class="valide">
      <h2 class="comp-title">C19</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Mettre en place son environnement d'apprentissage personnel</h3>
    <p>
      Configuration d'un environnement de développement complet avec VS Code,
      IntelliJ IDEA et GitHub…
    </p>
    <p class="rea-desc">Environnement perso — BTS SIO 2 ans</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog20}
    onkeydown={(e) => e.key === "Enter" && openDialog20()}
  >
    <div class="valide">
      <h2 class="comp-title">C20</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Mettre en œuvre des outils et stratégies de veille informationnelle</h3>
    <p>
      Veille technologique régulière sur la computer vision via YouTube,
      GitHub et ingénieurs Alstom…
    </p>
    <p class="rea-desc">Veille tech — Personnel & Stage</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog21}
    onkeydown={(e) => e.key === "Enter" && openDialog21()}
  >
    <div class="valide">
      <h2 class="comp-title">C21</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Gérer son identité professionnelle</h3>
    <p>
      Présence numérique cohérente sur LinkedIn, GitHub et portfolio web…
    </p>
    <p class="rea-desc">Identité numérique — Personnel</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog22}
    onkeydown={(e) => e.key === "Enter" && openDialog22()}
  >
    <div class="valide">
      <h2 class="comp-title">C22</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Développer son projet professionnel</h3>
    <p>
      Construction progressive d'un projet pro du BTS SIO vers le cycle
      ingénieur Big Data & ML…
    </p>
    <p class="rea-desc">Projet pro — Personnel</p>
  </div>
</div>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog19}
  onclick={(e) => e.target === dialog19 && closeDialog19()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog19}>✕</button>
    <Bloc
      competences="Compétence 19 - Mettre en place son environnement d'apprentissage personnel"
      projectTitle="Configuration d'un environnement de développement complet — BTS SIO"
      date="2024 - 2026"
      contexte="Réalisation:"
    />
    <p>
      Au cours de mes 2 ans de BTS SIO, j'ai configuré un environnement de
      développement complet adapté à mes projets personnels et de formation.
    </p>
    <ul class="tp-list">
      <li>VS Code comme IDE principal pour mes projets web et Python</li>
      <li>IntelliJ IDEA pour mes projets Java</li>
      <li>GitHub pour versionner l'ensemble de mes projets</li>
      <li>XAMPP pour héberger la base de données en local et les projets PHP</li>
      <li>Terminal intégré avec git, npm et maven</li>
      <li>Documentation des projets via README sur GitHub</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      GitHub Student m'a donné accès à des outils professionnels (IDEs, services
      cloud) gratuitement, ce qui m'a permis de travailler dans de bonnes
      conditions tout au long de la formation.
    </p>
    <ProjetAssocie projets={[
      { nom: "Projets personnels", contexte: "Personnel · 2024-2026" },
      { nom: "Projets de formation", contexte: "Formation · 2024-2026" }
    ]} />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <div class="proof-grid">
        <div class="proof-item">
          <img src="/vscode.png" alt="VS Code environment" />
          <p class="proof-caption">Environnement VS Code</p>
        </div>
        <div class="proof-item">
          <img src="/githubscreenshot.png" alt="GitHub repositories" />
          <p class="proof-caption">GitHub — Repositories</p>
        </div>
      </div>
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog20}
  onclick={(e) => e.target === dialog20 && closeDialog20()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog20}>✕</button>
    <Bloc
      competences="Compétence 20 - Mettre en œuvre des outils et stratégies de veille informationnelle"
      projectTitle="Veille technologique sur la computer vision"
      date="2024 - 2026"
      contexte="Réalisation:"
    />
    <p>
      J'ai mis en place une veille technologique régulière via plusieurs canaux
      tout au long de ma formation.
    </p>
    <ul class="tp-list">
      <li>Échanges avec des ingénieurs d'Alstom sur les sujets d'automatisation et de data</li>
      <li>Suivi de cours sur YouTube (Université de Stanford) sur la computer vision</li>
      <li>GitHub Alerts pour suivre les nouvelles publications dans mon domaine de veille</li>
      <li>Sujet principal : la computer vision et ses applications concrètes en entreprise</li>
      <li>Exemple notable : la RATP utilise la computer vision pour détecter les graffitis</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      La veille technologique est quelque chose que j'apprécie particulièrement
      car elle me permet de rester informé sur des sujets qui me passionnent,
      notamment la data science et ses applications concrètes en entreprise.
    </p>
    <ProjetAssocie projets={[
      { nom: "Veille technologique", contexte: "Personnel · 2024-2026" }
    ]} />
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog21}
  onclick={(e) => e.target === dialog21 && closeDialog21()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog21}>✕</button>
    <Bloc
      competences="Compétence 21 - Gérer son identité professionnelle"
      projectTitle="Présence numérique cohérente sur 3 plateformes"
      date="2024 - 2026"
      contexte="Réalisation:"
    />
    <p>
      J'ai maintenu une identité professionnelle cohérente sur 3 plateformes
      tout au long de ma formation.
    </p>
    <ul class="tp-list">
      <li>LinkedIn : profil complet avec mes expériences et projets des 2 ans de BTS</li>
      <li>GitHub : repositories publics de mes projets personnels et de formation</li>
      <li>Portfolio web : vitrine de mes projets et compétences</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      J'ai veillé à garder une cohérence dans mon identité numérique sur
      l'ensemble de ces 3 plateformes, avec un message et une image
      professionnelle unifiés.
    </p>
    <ProjetAssocie projets={[
      { nom: "Portfolio web", contexte: "Personnel · 2025" },
      { nom: "GitHub", contexte: "Personnel · 2024-2026" }
    ]} />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <div class="proof-grid">
        <div class="proof-item">
          <img src="/Screenshot_5.png" alt="LinkedIn profil" />
          <p class="proof-caption">LinkedIn — Profil professionnel</p>
        </div>
        <div class="proof-item">
          <img src="/githubscreenshot.png" alt="GitHub profil" />
          <p class="proof-caption">GitHub — Repositories publics</p>
        </div>
      </div>
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog22}
  onclick={(e) => e.target === dialog22 && closeDialog22()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog22}>✕</button>
    <Bloc
      competences="Compétence 22 - Développer son projet professionnel"
      projectTitle="Construction d'un projet professionnel orienté Big Data & MLOps"
      date="2024 - 2026"
      contexte="Réalisation:"
    />
    <p>
      J'ai construit mon projet professionnel progressivement au fil de la
      formation, avec des objectifs à court, moyen et long terme.
    </p>
    <ul class="tp-list">
      <li>Court terme (2026) : Obtenir le BTS SIO SLAM avec d'excellents résultats</li>
      <li>Moyen terme (2027) : Intégrer le cycle ingénieur Big Data & Machine Learning à l'EFREI en alternance</li>
      <li>Long terme : Se spécialiser en MLOps — automatisation appliquée au machine learning</li>
      <li>Montée en compétences sur les librairies ML : PyTorch, TensorFlow, scikit-learn</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Ma direction est claire : toujours dans l'automatisation, mais cette
      fois-ci appliquée au machine learning, afin d'apporter de nouvelles
      solutions à forte valeur ajoutée en entreprise.
    </p>
    <ProjetAssocie projets={[
      { nom: "Projet professionnel", contexte: "Personnel · 2024-2026" }
    ]} />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <div class="proof-grid">
        <div class="proof-item">
          <img src="/Screenshot_5.png" alt="LinkedIn profil et parcours" />
          <p class="proof-caption">LinkedIn — Profil et parcours</p>
        </div>
      </div>
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
  .proof-item img { max-width: 100%; border-radius: 6px; }
  .proof-caption {
    font-family: var(--ibm);
    font-size: 11px;
    color: rgba(255, 255, 255, 0.5);
    text-align: center;
    margin: 0;
  }
</style>
