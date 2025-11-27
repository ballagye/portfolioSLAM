<script lang="ts">
  let { title } = $props();
</script>

<div id="section-header" class="sectionheaderbts">
  <h3 class="heading">{title}</h3>
</div>

<style>
  .heading {
    font-family: "SF Pro Display", sans-serif;
    color: oklch(96.2% 0.018 272.314);
    font-size: 30px;
    font-weight: 700;
  }

  #section-header {
    display: flex;
    flex-direction: row;
    width: 100%;
    margin: 0px;
    padding: 0;
  }

  .heading::after {
    content: "";
    display: inline-flex;
    align-items: center;
    justify-content: center;
    position: relative;
    top: -10px;
    width: 300px;
    height: 1px;
    margin-left: 25px;
    background-color: var(--lightest-indigo);
  }
</style>
