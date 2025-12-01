<script lang="ts">
  import SectionHeader from "./SectionHeader.svelte";
  import { Tabs } from "bits-ui";
</script>

<section class="experience-section">
  <div class="section-header">
    <SectionHeader title={"/ Expérience"} />
  </div>
  <div class="tabs">
    <Tabs.Root
      value="alstom"
      data-tabs-root
      style="display: flex;
      align-items: center;
      gap: 50px;"
    >
      <Tabs.List
        style="display: grid; 
      gap: 10px"
      >
        <Tabs.Trigger value="alstom">
          {#snippet child({ props })}
            <button {...props} class="scoped-button"> Alstom</button>
          {/snippet}

          Alstom</Tabs.Trigger
        >
        <Tabs.Trigger value="saigon">
          {#snippet child({ props })}
            <button {...props} class="scoped-button"> SAIGON</button>
          {/snippet}

          Saigon</Tabs.Trigger
        >
      </Tabs.List>
      <Tabs.Content value="alstom">
        <div class="alstom-content">
          <h3>
            <span>Stage DevOps (Python, Ansible)</span>
            <span class="at"> @ </span>
            <a href="https://www.alstom.com/fr" target="_blank" class="company">
              Alstom</a
            >
          </h3>
          <p>Mai 2025 - Juillet 2025</p>
          <ul>
            <li>foo</li>
            <li>foo</li>
            <li>foo</li>
            <li>foo</li>
          </ul>
        </div>
      </Tabs.Content>
      <Tabs.Content value="saigon">
        <div class="saigon-content">
          <h3>
            <span>Stage</span>
            <span class="at"> @ </span>
            <a href="" target="_blank" class="company"> SAIGON</a>
          </h3>
          <p>Novembre 2025 - Décembre 2025</p>
          <ul>
            <li>foo</li>
            <li>foo</li>
            <li>foo</li>
            <li>foo</li>
          </ul>
        </div>
      </Tabs.Content>
    </Tabs.Root>
  </div>
</section>

<style>
  .experience-section {
    margin: 0px auto;
    max-width: 1100px;
  }
  h3 {
    font-family: var(--sfpro);
    color: var(--light-indigo);
    margin-bottom: 8px;
    font-size: 20px;
  }
  .company {
    position: relative;
    text-decoration: none;
    color: var(--blue);
  }
  .company:hover {
    scale: 1.2;
    text-decoration: underline;
    text-decoration-thickness: 1px;
    text-underline-offset: 4px;
  }
  .at {
    text-decoration: none;
    color: var(--blue);
  }
  p {
    font-family: var(--ibm);
    color: var(--light-indigo2);
    font-size: 14px;
    margin-bottom: 25px;
    margin: 0px;
  }
  .scoped-button {
    background-color: transparent;
    background-repeat: no-repeat;
    border: none;
    cursor: pointer;
    overflow: hidden;
    outline: none;
    font-size: var(--fz-xs);
    font-family: var(--ibm);
    color: var(--light-indigo2);
    padding: 0px 20px 2px;
    border-right: 2px solid;
    height: var(--tab-height);
  }
  [data-tabs-trigger][data-state="active"] {
    color: var(--blue);
  }
</style>
