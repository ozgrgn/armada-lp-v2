<script>
  import { useLocation } from "svelte-navigator";
  import "../assets/global.css";
  import { region } from "../services/store";
    let location = useLocation();
  region.set( 
    $location?.pathname?.split("/") &&
      $location?.pathname?.split("/")[1].length> 0
      ? $location?.pathname?.split("/")[1]
      : "uk"
  );
  console.log( $location?.pathname?.split("/").length)
</script>

{#await import("./MobBanner.svelte") then component}
  <svelte:component this={component.default} />
{/await}

{#await import("./MobCarousel.svelte") then component}
  <svelte:component this={component.default} />
{/await}

{#await import("./MobFeatures.svelte") then component}
  <svelte:component this={component.default} />
{/await}
{#await import("./MobPrices.svelte") then component}
  <svelte:component this={component.default} />
{/await}
{#await import("./MobDark.svelte") then component}
  <svelte:component this={component.default} />
{/await}