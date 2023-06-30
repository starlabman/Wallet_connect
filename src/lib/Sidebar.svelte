<script lang="ts">
  import Wallet from "./Wallet.svelte";
</script>

<style lang="scss">
  .sidebar {
    height: 100%;
    display: grid;
    grid-template-rows: 20% 60% 20%;
    gap: 20px;

    .sidebar__dex {
      display: flex;
      flex-direction: column;
      justify-content: center; /* Centrer horizontalement */
      align-items: center; /* Centrer verticalement */
      gap: 10px;

      button {
        width: 80%;
      }
    }

    .sidebar__footer {
      text-align: center;
    }
  }

  @media screen and (max-height: 700px) {
    .sidebar {
      height: calc(100% - (20px * 2));
    }
  }
</style>

<aside class="sidebar">
  <div class="sidebar__dex">
    <div style="flex-grow: 1;"></div> <!-- Espace vide pour centrer verticalement -->
    <Wallet />
    <div style="flex-grow: 1;"></div> <!-- Espace vide pour centrer verticalement -->
  </div>

  <div class="sidebar__footer">Build by starlabman</div>
</aside>
