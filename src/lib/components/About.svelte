<script>
  import SectionHeader from "./SectionHeader.svelte";
</script>

<section class="about-section">
  <div class="section-header">
    <SectionHeader title={"/ A propos"} />
  </div>
</section>

<style>
  .about-section {
    margin: 0px auto;
    max-width: 1100px;
  }
  .section-header {
    display: flex;
    flex-direction: row;
    width: 100%;
    margin: 0px;
    padding: 0;
  }
</style>
