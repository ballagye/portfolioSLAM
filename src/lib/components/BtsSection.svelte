<script lang="ts">
  import SectionHeader from "./SectionHeader.svelte";
  import Images from "./Images.svelte";
  import SlamImage from "./SlamImage.svelte";
  import { ServerCog } from "@jis3r/icons";
  import { SquareTerminal } from "@jis3r/icons";
  import { ChevronsLeftRight } from "@jis3r/icons";
  import { ChartNoAxesGantt } from "@jis3r/icons";
  import { fly } from "svelte/transition";
  import { sineOut } from "svelte/easing";
  import { onMount } from "svelte";

  let techlist: HTMLElement | null = null;
  let visible = false;

  onMount(() => {
    if (!techlist) return;
    const observer = new IntersectionObserver((entries) => {
      const entry = entries[0];
      if (entry.isIntersecting) {
        visible = true;
      }
    });
    observer.observe(techlist);
    return () => observer.disconnect();
  });
  const sisrTechList = [
    "Machine Virtuelles",
    "Linux",
    "Debian",
    "Ubuntu",
    "Windows Server",
  ];

  const slamTechList = [
    "VS Code",
    "Java",
    "Python",
    "Web",
    "SQL",
    "PHP",
    "JavaScript",
  ];
</script>

<section id="bts-sio">
  <div class="section-header"><SectionHeader title={"/ BTS SIO"} /></div>
  <div class="bts-desc">
    <p>
      Le Brevet de Technicien Supérieur aux Services Informatiques aux
      Organisations (BTS SIO) est un programme de niveau Bac+2 et s’adresse aux
      personnes qui souhaitent se former en deux ans aux métiers d’<span
        class="colored"
        >administrateurs réseau
      </span>
      ou de <span class="colored">développeur</span>.
    </p>
    <br />
    <p>
      Il peut-être réalisable soit en <span class="colored">alternance </span>
      d’une durée de 12 ou de 24 ou alors en
      <span class="colored"> initial </span> un minimum de 10 semaines de stages
      obligatoire en entreprise d’une durée de 2 à 3 mois, afin de s’initier aux
      réalités du domaine professionnel.
    </p>
    <br />
    <p>
      <b
        >Le BTS SIO propose deux <span class="colored"> spécialités</span> :
      </b>
    </p>
  </div>
  <div class="sisr">
    <div class="sisr-content">
      <div>
        <p class="overline">SISR</p>
        <h3 class="option-title">Réseaux</h3>
        <ul class="options-list">
          <li>
            Gestion des <span class="colored"> systèmes d’exploitation</span> et
            des services réseaux
          </li>
          <li>
            Gestion et la maintenance des infrastructures <span class="colored"
              >réseau</span
            >
          </li>
          <li>
            Optimisation des <span class="colored"
              >performances d’un réseau</span
            >
          </li>
          <li>
            <span class="colored">Sécurisations</span> des infrastructures
          </li>
        </ul>
        <ul class="sisr-tech-list">
          {#each sisrTechList as sisrList}
            <li>
              {sisrList}
            </li>
          {/each}
        </ul>
        <div class="logos">
          <div class="sisr-logo"><ServerCog /></div>
          <div class="sisr-logo"><SquareTerminal /></div>
        </div>
      </div>
    </div>
    <div class="sisr-image"><Images /></div>
  </div>

  <div class="slam">
    <div class="slam-content">
      <div>
        <p class="slam-overline">SLAM</p>
        <h3 class="option-title-slam">Développment</h3>
        <ul class="slam-options-list">
          <li>
            Développer des compétences en développement d’<span class="colored"
              >applications
            </span>
            et de
            <span class="colored">logiciels </span>
          </li>
          <li>
            Conception des <span class="colored"> bases de données </span>
          </li>
          <li>
            <span class="colored">Programmation </span> dans divers langages
          </li>
          <li>
            Tests et déploiement des <span class="colored"
              >solutions logicielles</span
            >
          </li>
        </ul>
        <ul bind:this={techlist} class="slam-tech-list">
          {#each slamTechList as slamList}
            {#if visible}
              <li transition:fly={{ x: 100, duration: 500, easing: sineOut }}>
                {slamList}
              </li>
            {/if}
          {/each}
        </ul>
        <div class="logos-slam">
          <div class="slam-logo"><ChevronsLeftRight /></div>
          <div class="slam-logo"><ChartNoAxesGantt /></div>
        </div>
      </div>
    </div>
    <div class="slam-image"><SlamImage /></div>
  </div>
</section>

<style>
  p {
    margin: 0px 25px 0px 0px;
    font-family: "SF Pro Display", sans-serif;
    font-size: 18px;
    color: oklch(96.2% 0.018 272.314);
    font-family: "SF Pro Display", sans-serif;
  }

  #bts-sio {
    margin: 0px auto;
    max-width: 1500px;
  }
  .sisr {
    display: grid;
    align-items: center;
    justify-content: center;
    gap: 10px;
    grid-template-columns: repeat(12, 1fr);
    margin-bottom: 100px;
  }
  .sisr-content {
    position: relative;
    grid-column: 7 / -1;
    grid-row-start: 1;
    grid-row-end: -1;
  }
  .sisr-image {
    position: relative;
    grid-column: 1 / 8;
    grid-row-start: 1;
    grid-row-end: -1;
  }
  .options-list {
    list-style: none;
    background-color: var(--dark-indigo);
    position: relative;
    padding: 15px 47px;
    z-index: 4;
    border-radius: 2px;
    font-family: var(--sfpro);
    color: var(--light-indigo2);
    font-weight: 400;
    font-size: 20px;
  }

  .bts-desc {
    width: 100vw;
    max-width: 1500px;
    margin: 0 auto;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
    margin-bottom: 111px;
  }
  .section-header {
    width: 100vw;
    max-width: 1500px;
    margin: 0 auto;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
  }
  .colored {
    color: var(--blue);
  }
  ul {
    margin: 0;
  }
  .overline {
    margin: 10px 0px;
    text-align: right;
    font-family: var(--ibm);
    color: var(--blue);
  }
  .option-title {
    text-align: right;
    font-family: var(--sfpro);
    color: var(--light-indigo);
    margin: 0px 0px 20px;
  }
  .sisr-tech-list {
    position: relative;
    display: flex;
    justify-content: flex-end;
    flex-wrap: wrap;
    gap: 17px;
    list-style: none;
    margin: 25px 0px 10px;
    padding: 0px;
    z-index: 2;
    font-family: var(--ibm);
    color: var(--light-indigo2);
    font-size: 15px;
  }

  .options-list li::before {
    content: "▹";
    position: absolute;
    left: 17px;
    color: var(--blue);
  }
  .slam-options-list li::before {
    content: "▹";
    position: absolute;
    left: 17px;
    color: var(--blue);
  }

  .sisr-logo {
    color: var(--light-indigo);
  }
  .sisr-logo:hover {
    color: var(--blue);
  }
  .logos {
    display: flex;
    justify-content: flex-end;
    gap: 10px;
    margin-top: 10px;
  }
  .slam {
    display: grid;
    align-items: center;
    justify-content: center;
    gap: 10px;
    grid-template-columns: repeat(12, 1fr);
    margin-bottom: 100px;
  }
  .slam-content {
    position: relative;
    grid-area: 1 / 1 / -1 / 7;
  }
  .slam-image {
    grid-area: 1/ 6 / -1 / -1;
    position: relative;
  }
  .slam-options-list {
    list-style: none;
    background-color: var(--dark-indigo);
    position: relative;
    padding: 15px 47px;
    font-size: 13px;

    z-index: 4;
    border-radius: 2px;
    font-family: var(--sfpro);
    color: var(--light-indigo2);
    font-weight: 400;
    font-size: 20px;
  }
  .slam-overline {
    margin: 10px 0px;
    text-align: left;
    font-family: var(--ibm);
    color: var(--blue);
  }
  .option-title-slam {
    text-align: left;
    font-family: var(--sfpro);
    color: var(--light-indigo);
    margin: 0px 0px 20px;
  }
  .slam-tech-list {
    position: relative;
    display: flex;
    justify-content: left;
    flex-wrap: wrap;
    gap: 17px;
    list-style: none;
    margin: 25px 0px 10px;
    padding: 0px;
    z-index: 4;
    font-family: var(--ibm);
    color: var(--light-indigo2);
    font-size: 15px;
  }
  .logos-slam {
    display: flex;
    justify-content: left;
    gap: 10px;
    margin-top: 10px;
    color: var(--light-indigo);
  }

  .slam-logo:hover {
    color: var(--blue);
  }
  .sisr-image::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 99%;

    z-index: 3;
    transition: var(--transition);
    background-color: var(--dark-blue);
    mix-blend-mode: screen;
    border-radius: var(--border-radius);
    vertical-align: middle;
  }
  .sisr-image:hover::before {
    background: transparent;
  }
  .slam-image::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 99%;
    inset: 0px;
    z-index: 3;
    transition: var(--transition);
    background-color: var(--dark-blue);
    mix-blend-mode: screen;
    border-radius: var(--border-radius);
    vertical-align: middle;
  }
  .slam-image:hover::before {
    background: transparent;
  }
</style>
