<script>
  import { Copyright } from "@lucide/svelte";
</script>

<footer class="footer">
  <p>2025 <Copyright size="13" /> Balla Gueye</p>
</footer>

<style>
  p {
    font-family: var(--ibm);
    color: var(--light-indigo2);
  }

  .footer {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: auto;
    min-height: 70px;
    padding: 15px;
    text-align: center;
  }
</style>
