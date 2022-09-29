<script>
  import { useLocation } from "svelte-navigator";
  import { perma } from "../services/store";
  import { region } from "../services/store";
  import Banner2 from "./Banner2.svelte";
  import Dark from "./Dark.svelte";
  import Features from "./Features.svelte";
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

<Banner2 />
<Features />

<Dark />
