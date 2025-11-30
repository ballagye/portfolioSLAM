<script lang="ts">
  import SectionHeader from "./SectionHeader.svelte";
  import { Tabs } from "bits-ui";
</script>

<section class="experience-section">
  <div class="section-header">
    <SectionHeader title={"/ Expérience"} />
  </div>
  <div class="tabs">
    <Tabs.Root value="alstom">
      <Tabs.List class="tabs-list">
        <Tabs.Trigger value="alstom">Alstom</Tabs.Trigger>
        <Tabs.Trigger value="saigon">Saigon</Tabs.Trigger>
      </Tabs.List>
      <Tabs.Content value="alstom">
        <div class="alstom-content">
          <h3>
            <span>Stage</span>
            <span>
              @<a href="https://www.alstom.com/fr" target="_blank">
                Alstom</a
              ></span
            >
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
      <Tabs.Content value="saigon">
        <div class="saigon-content">
          <h3>
            <span>Stage</span>
            <span>@ <a href="blank"> SAIGON</a></span>
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
    </Tabs.Root>
  </div>
</section>

<style>
  .experience-section {
    margin: 0px auto;
    max-width: 1100px;
  }
</style>
