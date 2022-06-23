<script>
  import "../assets/global.css";
  import { useLocation } from "svelte-navigator";
  import { region } from "../services/store";
  let location = useLocation();
  region.set( 
    $location?.pathname?.split("/") &&
      $location?.pathname?.split("/")[1].length> 0
      ? $location?.pathname?.split("/")[1]
      : "uk"
  );
</script>

{#await import("./Banner2.svelte") then component}
  <svelte:component this={component.default} />
{/await}

{#await import("./Features.svelte") then component}
  <svelte:component this={component.default} />
{/await}

{#await import("./Pricelist.svelte") then component}
  <svelte:component this={component.default} />
{/await}
{#await import("./Dark.svelte") then component}
  <svelte:component this={component.default} />
{/await}

