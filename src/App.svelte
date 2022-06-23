<script>
  import { Router, Route } from "svelte-navigator";
  import Navbar from "./common/Navbar.svelte";
  import Footer from "./common/Footer.svelte";
  import Policy from "./common/Policy.svelte";
  import { onMount } from "svelte";

  onMount(() => {
    setTimeout(() => {
      var s = document.createElement("script");
      s.type = "text/javascript";
      s.src = "http://code.jivosite.com/widget/wGPM2QDpTj";
      document.head.appendChild(s);
    }, 5000);
  });

  const mobileDetector = () => {
    try {
      if (
        /Android|webOS|iPhone|iPad|iPod|pocket|psp|kindle|avantgo|blazer|midori|Tablet|Palm|maemo|plucker|phone|BlackBerry|symbian|IEMobile|mobile|ZuneWP7|Windows Phone|Opera Mini/i.test(
          navigator.userAgent
        )
      ) {
        return true;
      }
      return false;
    } catch (e) {
      console.log("Error in isMobile");
      return false;
    }
  };

  let isMobile = mobileDetector();
</script>

<main>
  <Navbar />

  <Router>
    <Route path="policy" component={Policy}><Policy /></Route>
    {#if isMobile}
      <Route path="/*">
        {#await import("./mobile/Mobile.svelte") then component}
          <svelte:component this={component.default} />
        {/await}
      </Route>
    {:else}
      <Route path="/*">
        {#await import("./web/Web.svelte") then component}
          <svelte:component this={component.default} />
        {/await}
      </Route>
    {/if}
  </Router>
  <Footer />
</main>
