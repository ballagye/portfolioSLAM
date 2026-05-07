<script lang="ts">
  let { projets } = $props();
</script>

<div class="projets">
  <p class="projets-header">Projet(s) associé(s)</p>
  {#each projets as projet}
    <div class="projet-item">
      <span class="projet-nom">{projet.nom}</span>
      <span class="projet-contexte">{projet.contexte}</span>
    </div>
  {/each}
</div>

<style>
  .projets {
    margin: 16px 0;
  }
  .projets-header {
    color: var(--blue);
    font-family: var(--ibm);
    font-weight: 700;
    font-size: 12px;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    margin-bottom: 8px;
  }
  .projet-item {
    display: flex;
    align-items: center;
    gap: 12px;
    background: rgba(255, 255, 255, 0.04);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 6px;
    padding: 10px 14px;
    margin-bottom: 6px;
  }
  .projet-nom {
    flex: 1;
    font-family: var(--sfpro);
    font-size: 14px;
    margin: 0;
  }
  .projet-contexte {
    font-family: var(--ibm);
    font-size: 12px;
    color: var(--blue);
    white-space: nowrap;
  }
</style>
