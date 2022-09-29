<script>
  import { useLocation } from "svelte-navigator";
  import { region } from "../services/store";
  import MobBanner from "./MobBanner.svelte";
  import MobCarousel from "./MobCarousel.svelte";
  import MobDark from "./MobDark.svelte";
  import MobFeatures from "./MobFeatures.svelte";
  import MobPrices from "./MobPrices.svelte";
  let location = useLocation();
  region.set(
    $location?.pathname?.split("/") &&
      $location?.pathname?.split("/")[1].length > 0
      ? $location?.pathname?.split("/")[1]
      : "uk"
  );
  console.log($location?.pathname?.split("/").length);
</script>

<MobBanner />

<MobCarousel />

<MobFeatures />



<MobDark />
