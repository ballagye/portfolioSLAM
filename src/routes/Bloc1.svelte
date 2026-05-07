<script lang="ts">
  import Bloc from "../lib/components/Bloc.svelte";
  import ProjetAssocie from "../lib/components/ProjetAssocie.svelte";
  import { MoveUpRight } from "@lucide/svelte";

  let dialog: HTMLDialogElement | undefined = undefined;
  let dialog2: HTMLDialogElement | undefined = undefined;
  let dialog3: HTMLDialogElement | undefined = undefined;

  function openDialog() {
    dialog?.showModal();
  }
  function closeDialog() {
    dialog?.close();
  }
  function openDialog2() {
    dialog2?.showModal();
  }
  function closeDialog2() {
    dialog2?.close();
  }
  function openDialog3() {
    dialog3?.showModal();
  }
  function closeDialog3() {
    dialog3?.close();
  }
  let dialog4: HTMLDialogElement | undefined = undefined;
  function openDialog4() {
    dialog4?.showModal();
  }
  function closeDialog4() {
    dialog4?.close();
  }
  let dialog5: HTMLDialogElement | undefined = undefined;
  function openDialog5() {
    dialog5?.showModal();
  }
  function closeDialog5() {
    dialog5?.close();
  }
  let dialog6: HTMLDialogElement | undefined = undefined;
  function openDialog6() {
    dialog6?.showModal();
  }
  function closeDialog6() {
    dialog6?.close();
  }
</script>

<div class="bloc-title">
  <h2>/ Bloc 1 Gérer le patrimoine informatique</h2>
</div>
<div class="competences-grid">
  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog}
    onkeydown={(e) => e.key === "Enter" && openDialog()}
  >
    <div class="valide">
      <h2 class="comp-title">C1</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Recenser et identifier les ressources numériques</h3>
    <p>
      Recenser et identifier les ressources numériques à l'aide d'un outil de
      gestion de parc…
    </p>
    <p class="rea-desc">Inventaire du parc GLPI -- Formation</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog2}
    onkeydown={(e) => e.key === "Enter" && openDialog2()}
  >
    <div class="valide">
      <h2 class="comp-title">C2</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Exploiter des référentiels, normes et standards</h3>
    <p>
      Exploiter des référentiels, normes et standards adoptés par le prestataire
      informatique…
    </p>
    <p class="rea-desc">Configuration GLPI / ITIL -- Formation</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog3}
    onkeydown={(e) => e.key === "Enter" && openDialog3()}
  >
    <div class="valide">
      <h2 class="comp-title">C3</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">
      Mettre en place et vérifier les niveaux d'habilitation
    </h3>
    <p>
      Mettre en place et vérifier les niveaux d'habilitation associés à un
      service…
    </p>
    <p class="rea-desc">Droits d'accès GLPI -- Formation</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog4}
    onkeydown={(e) => e.key === "Enter" && openDialog4()}
  >
    <div class="valide">
      <h2 class="comp-title">C4</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Mettre en place un outil de gestion des services</h3>
    <p>
      Déploiement et validation d'un outil d'automatisation sur projets
      ferroviaires réels…
    </p>
    <p class="rea-desc">Automatisation Excel -- Entreprise</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog5}
    onkeydown={(e) => e.key === "Enter" && openDialog5()}
  >
    <div class="valide">
      <h2 class="comp-title">C5</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">Gérer les sauvegardes</h3>
    <p>
      Génération et archivage des fichiers de configuration des switchs réseau…
    </p>
    <p class="rea-desc">Sauvegardes switchs -- Alstom</p>
  </div>

  <div
    class="competences"
    role="button"
    tabindex="0"
    onclick={openDialog6}
    onkeydown={(e) => e.key === "Enter" && openDialog6()}
  >
    <div class="valide">
      <h2 class="comp-title">C6</h2>
      <MoveUpRight />
    </div>
    <h3 class="rea-title">
      Vérifier le respect des règles d'utilisation des ressources numériques
    </h3>
    <p>
      Audit et correction des règles d'usage lors de la refonte d'un site
      vitrine…
    </p>
    <p class="rea-desc">Conformité web -- Entreprise</p>
  </div>
</div>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog2}
  onclick={(e) => e.target === dialog2 && closeDialog2()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog2}>✕</button>
    <Bloc
      competences="Compétence 2 - Exploiter des référentiels, normes et standards adoptés par le prestataire informatique"
      projectTitle="Configuration des règles de gestion des incidents dans GLPI selon le référentiel ITIL"
      date="Octobre 2025"
      contexte="Réalisation:"
    />
    <p>
      Dans le cadre d'un TP sur GLPI, j'ai configuré une instance en appliquant
      les bonnes pratiques du référentiel ITIL pour structurer la gestion des
      incidents au sein d'une entreprise fictive.
    </p>

    <ul class="tp-list">
      <li>
        Définition de 4 niveaux de priorité selon la matrice urgence/impact ITIL
        : Très haute, Haute, Moyenne, Basse
      </li>
      <li>
        Création de tickets d'incidents types : panne réseau (Très haute), accès
        refusé à un logiciel (Haute)
      </li>
      <li>Catégorisation de chaque ticket selon son type de problème</li>
      <li>
        Attribution des tickets aux techniciens compétents selon la catégorie
      </li>
    </ul>

    <p class="section-title">Bilan</p>
    <p>
      La création du référentiel a été assez intuitive à mettre en place. J'ai
      dû consulter la documentation GLPI pour configurer les bonnes règles de
      gestion des tickets et appliquer les bonnes pratiques ITIL. Cela m'a
      appris à me documenter de manière autonome pour configurer correctement
      un outil professionnel.
    </p>
    <ProjetAssocie
      projets={[
        {
          nom: "Mise en place d'un environnement GLPI",
          contexte: "Formation · Oct 2025",
        },
      ]}
    />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img src="/Screenshot_2.png" alt="Preuve ITIL GLPI" />
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog}
  onclick={(e) => e.target === dialog && closeDialog()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog}>✕</button>
    <Bloc
      competences="Compétence 1 - Recenser et identifier les ressources numériques"
      projectTitle="Installation et configuration de GLPI"
      date="Octobre 2025"
      contexte="Réalisation:"
    />
    <p>
      J'ai installé et configuré GLPI sur une machine virtuelle Debian pour
      automatiser le recensement du parc informatique.
    </p>
    <ul class="tp-list">
      <li>Installation de l'environnement serveur : Apache, MariaDB, PHP</li>
      <li>Déploiement de GLPI et configuration de la base de données</li>
      <li>Mise en place de l'agent d'inventaire sur les postes clients</li>
      <li>
        Remontée automatique des informations matérielles et logicielles dans
        GLPI
      </li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      La mise en place a demandé du temps, notamment pour comprendre le
      fonctionnement de l'agent GLPI et sa remontée des données. En groupe, nous
      avons fini par réussir à inventorier l'ensemble du parc avec les adresses
      IP via l'agent. Cette expérience m'a appris l'importance d'un référentiel
      centralisé pour gérer un parc informatique.
    </p>
    <ProjetAssocie
      projets={[
        {
          nom: "Mise en place d'un environnement GLPI",
          contexte: "Formation · Oct 2025",
        },
      ]}
    />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img src="/image.png" alt="Preuve GLPI" />
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog3}
  onclick={(e) => e.target === dialog3 && closeDialog3()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog3}>✕</button>
    <Bloc
      competences="Compétence 3 - Mettre en place et vérifier les niveaux d'habilitation associés à un service"
      projectTitle="Configuration des droits d'accès et des rôles utilisateurs dans GLPI"
      date="Octobre 2025"
      contexte="Réalisation:"
    />
    <p>
      J'ai configuré les niveaux d'accès des utilisateurs dans GLPI en
      attribuant un profil adapté à chaque rôle.
    </p>
    <ul class="tp-list">
      <li>
        8 profils définis : Self-Service, Observer, Hotliner, Technician,
        Supervisor, Admin, Super-Admin, Read-Only
      </li>
      <li>Droits ajustés pour chaque profil selon son périmètre d'action</li>
      <li>Tests de connexion pour valider les accès de chaque profil</li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      La configuration des droits d'accès par rôle dans GLPI s'est révélée
      assez intuitive à mettre en place. J'ai appliqué les bonnes pratiques en
      attribuant à chaque profil uniquement les permissions nécessaires à sa
      fonction, ce qui m'a permis de comprendre l'importance du principe du
      moindre privilège en entreprise.
    </p>
    <ProjetAssocie
      projets={[
        { nom: "Droits d'accès GLPI", contexte: "Formation · Oct 2025" },
      ]}
    />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img src="/Screenshot_1.png" alt="Preuve habilitations GLPI" />
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog4}
  onclick={(e) => e.target === dialog4 && closeDialog4()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog4}>✕</button>
    <Bloc
      competences="Compétence 4 - Vérification des conditions de la continuité d'un service"
      projectTitle="Automatisation de l'import de données Excel sur projets ferroviaires"
      date="Mai - Juillet 2025"
      contexte="Réalisation:"
    />
    <p>
      J'ai validé mon outil d'automatisation en le testant sur deux projets
      ferroviaires réels chez Alstom : la ligne de Turin et la ligne du Caire.
    </p>
    <ul class="tp-list">
      <li>
        Import des données Excel sur la ligne de Turin et vérification des
        résultats
      </li>
      <li>
        Même test sur la ligne du Caire pour valider la généricité de l'outil
      </li>
      <li>
        Recueil des retours des ingénieurs réseau pour identifier les
        ajustements
      </li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Cette mission de gestion des sauvegardes m'a permis de valider la
      compétence en contexte professionnel réel. Les retours positifs des
      ingénieurs réseau et de mon tuteur, ainsi que l'utilisation du script sur
      plusieurs projets ferroviaires, confirment que la solution de sauvegarde
      centralisée répond bien au besoin de l'équipe.
    </p>
    <ProjetAssocie
      projets={[
        {
          nom: "Développement script Python HPE",
          contexte: "Stage Alstom · 2025",
        },
        {
          nom: "Extraction données Excel avec pandas",
          contexte: "Stage Alstom · 2025",
        },
      ]}
    />
    <div class="proof">
      <p class="proof-label">Démonstration</p>
      <img
        src="/Screenshot_3.png"
        alt="Preuve automatisation projets ferroviaires"
      />
    </div>
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog5}
  onclick={(e) => e.target === dialog5 && closeDialog5()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog5}>✕</button>
    <Bloc
      competences="Compétence 5 - Gérer les sauvegardes"
      projectTitle="Génération et archivage des fichiers de configuration des switchs réseau"
      date="Mai - Juillet 2025"
      contexte="Réalisation:"
    />
    <p>
      Durant mon stage chez Alstom, j'ai centralisé les fichiers de
      configuration des switchs HPE pour garantir leur traçabilité et faciliter
      les interventions futures.
    </p>
    <ul class="tp-list">
      <li>Collecte des fichiers .cfg de chaque switch HPE du projet</li>
      <li>Nommage structuré pour identifier rapidement chaque équipement</li>
      <li>
        Rédaction d'une documentation expliquant l'organisation et la procédure
        de restauration
      </li>
      <li>
        Dépôt sur SharePoint pour rendre les sauvegardes accessibles à toute
        l'équipe
      </li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Le script a connu plusieurs versions successives, toutes déposées sur
      SharePoint afin que les ingénieurs réseau puissent y accéder et les
      utiliser directement. Cette centralisation garantit que les configurations
      des switchs sont toujours sauvegardées et disponibles, quelle que soit
      l'évolution du script.
    </p>
    <ProjetAssocie
      projets={[
        {
          nom: "Archivage fichiers de configuration switchs HPE",
          contexte: "Stage Alstom · 2025",
        },
      ]}
    />
  </div>
</dialog>

<!-- svelte-ignore a11y_click_events_have_key_events a11y_no_noninteractive_element_interactions -->
<dialog
  bind:this={dialog6}
  onclick={(e) => e.target === dialog6 && closeDialog6()}
>
  <div class="dialog-inner">
    <button class="dialog-close" onclick={closeDialog6}>✕</button>
    <Bloc
      competences="Compétence 6 - Vérifier le respect des règles d'utilisation des ressources numériques"
      projectTitle="Audit et mise en conformité lors de la refonte d'un site vitrine"
      date="Novembre - Décembre 2025"
      contexte="Réalisation:"
    />
    <p>
      Lors de mon deuxième stage, j'ai identifié et corrigé des manquements aux
      règles d'utilisation des ressources numériques sur un site vitrine.
    </p>
    <ul class="tp-list">
      <li>Absence de copyright détectée — mentions ajoutées sur le site</li>
      <li>
        Polices non licenciées remplacées par des alternatives libres de droits
      </li>
      <li>
        Problèmes signalés directement aux membres de l'équipe en présentiel
      </li>
    </ul>
    <p class="section-title">Bilan</p>
    <p>
      Les corrections ont été intégrées dès la phase de refonte, garantissant la
      conformité du site sans retouche post-livraison.
    </p>
    <ProjetAssocie
      projets={[
        { nom: "Refonte site vitrine Svelte", contexte: "Stage 2 · 2025" },
      ]}
    />
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

  .proof img {
    max-width: 100%;
    border-radius: 6px;
  }
  .valide {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
</style>
