<script lang="ts">
  let { competences, projectTitle, date, contexte } = $props();
</script>

<div class="competences">
  <div class="border">
    <div class="competence-title">
      <h3>{competences}</h3>
    </div>
    <div class="project-title">
      <h4>{projectTitle}</h4>
    </div>
    <div class="date">
      <p>{date}</p>
    </div>
    <div class="description">
      <h4>{contexte}</h4>
    </div>
  </div>
</div>

<style>
  .competences {
    display: flex;
    font-family: var(--sfpro);
    justify-content: center;
    flex-direction: column;
  }
  .competence-title {
    font-family: inherit;
    color: oklch(96.2% 0.018 272.314);
    margin-top: 20px;
    margin-bottom: 20px;
  }
  .date p {
    font-family: var(--ibm);
    color: var(--blue);
    font-weight: 400;
  }
</style>
