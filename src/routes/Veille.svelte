<script lang="ts">
  import { LinkPreview } from "bits-ui";
  import SectionHeader from "../lib/components/SectionHeader.svelte";
  import { Info } from "@lucide/svelte";
</script>

<div class="veille">
  <div class="header-row">
    <SectionHeader title={"Veille Technologique"} />
    <LinkPreview.Root openDelay={100} closeDelay={200}>
      <LinkPreview.Trigger class="info-trigger">
        {#snippet child({ props })}
          <div {...props} class="info-trigger" role="none">
            <Info class="info-icon" />
          </div>
        {/snippet}
      </LinkPreview.Trigger>
      <LinkPreview.Content class="preview-content" sideOffset={8} side="bottom">
        <p class="preview-text">
          La veille technologique est un processus continu de surveillance et
          d'analyse des évolutions d'un domaine technologique, permettant de
          rester informé des dernières innovations, tendances et actualités afin
          d'anticiper les changements et maintenir ses compétences à jour.
        </p>
      </LinkPreview.Content>
    </LinkPreview.Root>
  </div>

  <h2>
    La <span class="colored">Computer Vision</span> : quand les machines apprennent
    à voir le monde
  </h2>
  <h3>Introduction</h3>
  <p>
    La <span class="colored">Computer Vision</span>, ou vision par ordinateur,
    est un domaine de l'informatique qui permet aux machines
    <span class="colored">d'analyser</span>, comprendre et interpréter des
    images et des vidéos, exactement comme le ferait un œil humain. Grâce aux
    <span class="colored">réseaux</span> de neurones et au
    <span class="colored"></span>deep learning, ces systèmes peuvent détecter
    des objets, reconnaître des visages, analyser des scènes en temps réel ou
    encore identifier des anomalies invisibles à l'œil nu.
    <br />
    <br />

    J'ai choisi ce sujet car il est au intervient dans plusieurs domaines qui
    m'intéressent directement : le
    <span class="colored">machine learning</span>,
    <span class="colored">le traitement de données</span>
    visuelles et les systèmes automatisés. Dans le cadre de ma future spécialisation
    en <span class="colored">Big Data et Machine Learning</span>
    à l'EFREI, la Computer Vision représente l'un des domaines les plus porteurs
    et les plus concrets de l'informatique aujourd'hui, des transports parisiens
    aux blocs opératoires, ses applications transforment déjà notre
    <span class="colored">quotidien</span>.
  </p>
  <h2>Contexte</h2>
  <h3>Un marché en explosion</h3>
  <p>
    Le marché mondial de la Computer Vision était évalué à 19,83 milliards de
    dollars en 2024 et devrait croître de près de 20 % par an dans les
    prochaines années. Dans le seul secteur de la santé, ce marché devrait
    passer de 3,48 milliards en 2025 à plus de 62 milliards de dollars d'ici
    2035.
  </p>
  <h3>Une technologie déjà dans notre quotidien</h3>
  <p>
    Reconnaissance faciale sur smartphone, détection d'obstacles dans les
    véhicules autonomes, contrôle qualité en usine, surveillance intelligente
    dans les transports : la Computer Vision est déjà partout, souvent sans que
    nous en soyons conscients.
  </p>
  <h3>Un encadrement réglementaire qui se construit</h3>
  <p>
    L'AI Act européen de 2024 classe certains systèmes de Computer Vision parmi
    les usages à haut risque, soumis à des obligations strictes de transparence
    et de contrôle humain.
  </p>
  <div class="sources">
    <div>
      <h2>Sources</h2>
      <ul class="source">
        <li>
          Médias spécialisés : LeMagIT, L'Usine Digitale, Viso.ai, Ultralytics
          Blog.
        </li>
        <li>Réseaux : LinkedIn, X.</li>
      </ul>
    </div>
    <div>
      <h2>Thèmes</h2>
      <div class="cards">Détection d'objets</div>
      <div class="cards">Vision Transformers</div>
      <div class="cards">Transports</div>
      <div class="cards">Détection d'objets</div>
    </div>
  </div>
</div>

<style>
  .veille {
    margin: 0 auto;
    max-width: 1500px;
  }

  .header-row {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 16px;
  }

  :global(.info-trigger) {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    background: none;
    border: none;
    cursor: default;
    pointer-events: none;
    padding: 0;
    color: inherit;
    opacity: 0.5;
    transition: opacity 150ms ease;
    flex-shrink: 0;
  }

  :global(.info-trigger:hover) {
    opacity: 1;
  }

  :global(.info-icon) {
    width: 16px;
    height: 16px;
    pointer-events: all;
    cursor: default;
  }

  :global(.preview-content) {
    background-color: var(--lightest-blue);
    border: 1px solid var(--border, #e5e7eb);
    border-radius: 10px;
    padding: 14px 16px;
    max-width: 320px;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
    z-index: 50;
  }

  :global(.preview-text) {
    font-family: var(--sfpro);
    font-size: 13px;
    line-height: 1.6;
    margin: 0;
    opacity: 0.85;
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
    margin-bottom: 30px;
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
  .sources {
    display: flex;
    flex-direction: row;
    gap: 100px;
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
</style>
