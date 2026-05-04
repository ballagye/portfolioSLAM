<script lang="ts">
  import SectionHeader from "./SectionHeader.svelte";
</script>

<div class="epreuve">
  <SectionHeader
    title={"Épreuve E6 : Conception et développement d'applications"}
  />

  <h3>Objectif</h3>
  <p>
    Cette épreuve évalue l'acquisition des compétences en
    <span class="colored">conception et développement d'applications</span>
    à travers deux situations professionnelles : une application web (client léger)
    et une application de bureau (client lourd).
  </p>
  <ul class="source">
    <li>Concevoir et développer une solution applicative</li>
    <li>
      Assurer la maintenance corrective ou évolutive d'une solution applicative
    </li>
    <li>Gérer les données</li>
  </ul>
  <div class="presentation">
    <div>
      <h3 class="none">Situation 1 — Client léger</h3>
      <ul class="situations">
        <li>Le client léger est une application web</li>
        <li>Préparation de 30 minutes suivie d'un entretien de 20 minutes</li>
        <li>Préparation d'une heure suivie d'un entretien de 20 minutes</li>
      </ul>
    </div>

    <div>
      <h3 class="none">Situation 2 — Client lourd</h3>
      <ul class="situations">
        <li>Le client léger est une application web</li>
        <li>Préparation de 30 minutes suivie d'un entretien de 20 minutes</li>
        <li>Préparation d'une heure suivie d'un entretien de 20 minutes</li>
      </ul>
    </div>
  </div>

  <h2>Documentation</h2>

  <h3 class="none">Situation 1 — Savora Web (Client léger)</h3>
  <p class="date">Janvier – Mars 2026</p>
  <p>
    <span class="colored">Savora Web</span> est un site vitrine de restaurant
    développé avec <span class="colored">Svelte</span>, permettant aux
    utilisateurs de consulter la carte et de réserver une table en ligne.
    L'application intègre une
    <span class="colored">authentification</span> sécurisée dans le formulaire
    de réservation, une architecture de base de données pensée pour la gestion
    du restaurant, et utilise <span class="colored">Drizzle</span> comme ORM pour
    l'accès aux données.
  </p>
  <ul class="source">
    <li>Authentification dans le formulaire de réservation</li>
    <li>Consultation de la carte et des informations du restaurant</li>
    <li>Réservation d'une table avec sélection de date</li>
    <li>Architecture base de données dédiée au restaurant</li>
    <li>Accès aux données via ORM Drizzle</li>
  </ul>
  <div class="tags">
    <span class="cards">Svelte</span>
    <span class="cards">Drizzle ORM</span>
    <span class="cards">MySQL</span>
    <span class="cards">MVC</span>
  </div>

  <h3 class="none">Situation 2 — Savora Admin (Client lourd)</h3>
  <p class="date">Février – Mars 2026</p>
  <p>
    <span class="colored">Savora Admin</span> est une application de bureau
    dédiée à la gestion des réservations effectuées sur le site web. Elle
    communique avec le site via une <span class="colored">API REST</span> afin
    de récupérer toutes les réservations et propose un
    <span class="colored">CRUD complet</span> : consultation des informations client,
    modification et annulation des réservations.
  </p>
  <ul class="source">
    <li>Récupération des réservations via API REST</li>
    <li>Affichage des informations client</li>
    <li>Modification d'une réservation</li>
    <li>Annulation d'une réservation</li>
  </ul>
  <div class="tags">
    <span class="cards">API REST</span>
    <span class="cards">CRUD</span>
    <span class="cards">Svelte</span>
  </div>
</div>

<style>
  .epreuve {
    margin: 0 auto;
    max-width: 1500px;
  }

  h2,
  h3,
  p {
    font-family: var(--sfpro);
  }

  .colored {
    color: var(--blue);
  }

  p {
    font-size: 18px;
    margin-bottom: 10px;
  }
  .situations {
    list-style: none;
    position: relative;
    padding: 15px 47px;
    font-size: 18px;
    font-family: var(--sfpro);
  }
  .date {
    font-size: 14px;

    margin-bottom: 8px;
  }

  h3::after {
    content: "";
    display: inline-flex;
    align-items: center;
    justify-content: center;
    position: relative;
    top: -7px;
    width: 300px;
    height: 1px;
    margin-left: 25px;
    background-color: var(--lightest-indigo);
  }

  .none::after {
    top: -7px;
    width: 300px;
    height: 0px;
    margin-left: 0px;
    background-color: var(--lightest-indigo);
  }

  ul {
    margin: 0;
  }
  li::before {
    content: "▹";
    position: absolute;
    left: 17px;
    color: var(--blue);
  }

  .source {
    list-style: none;
    position: relative;
    padding: 15px 47px;
    font-size: 18px;
    font-family: var(--sfpro);
  }

  .tags {
    margin-bottom: 30px;
  }

  .cards {
    display: inline-block;
    padding: 0.25rem 0.75rem;
    background: var(--indigo-dark);
    color: var(--white);
    border: 1px solid var(--blue);
    border-radius: 4px;
    font-size: 0.8rem;
    margin-right: 0.5rem;
    margin-bottom: 0.5rem;
    font-family: var(--sfpro);
  }
  .date {
    font-family: var(--ibm);
    color: var(--blue);
  }
  .presentation {
    display: flex;
    flex-direction: row;
    gap: 30px;
  }
</style>
