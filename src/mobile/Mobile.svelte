<script>
  import Reviews from "./Reviews.svelte";
  import { useLocation } from "svelte-navigator";
  import { perma } from "../services/store";
  import { region } from "../services/store";
  import MobBanner from "./MobBanner.svelte";
  import MobCarousel from "./MobCarousel.svelte";
  import MobDark from "./MobDark.svelte";
  import MobFeatures from "./MobFeatures.svelte";
  import MobPrices from "./MobPrices.svelte";
  let location = useLocation();
  perma.set(
    $location?.pathname?.split("/")[2] &&
      $location?.pathname?.split("/")[2].length > 0
      ? $location?.pathname?.split("/")[2]
      : "implant"
  );
  region.set(
    $location?.pathname?.split("/")[1] &&
      $location?.pathname?.split("/")[1].length > 0
      ? $location?.pathname?.split("/")[1]
      : "uk"
  );
  console.log($region)
  console.log($perma)
</script>

<MobBanner />

<MobCarousel />

<MobFeatures />

<Reviews />

<MobDark />
