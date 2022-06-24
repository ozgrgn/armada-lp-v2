<script>
  import { useLocation } from "svelte-navigator";
  import { region } from "../services/store";
  import Banner2 from "./Banner2.svelte";
  import Dark from "./Dark.svelte";
  import Features from "./Features.svelte";
  import Pricelist from "./Pricelist.svelte";
  let location = useLocation();
  region.set(
    $location?.pathname?.split("/") &&
      $location?.pathname?.split("/")[1].length > 0
      ? $location?.pathname?.split("/")[1]
      : "uk"
  );
</script>

<Banner2 />
<Features />
<Pricelist />
<Dark />
