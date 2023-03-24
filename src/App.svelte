<script>
  import { Router, Route } from "svelte-navigator";
  import Navbar from "./common/Navbar.svelte";
  import Footer from "./common/Footer.svelte";
  import Policy from "./common/Policy.svelte";
  import { onMount } from "svelte";
  import Mobile from "./mobile/Mobile.svelte";
  import Web from "./web/Web.svelte";

  onMount(() => {
    // setTimeout(() => {
    //   var s = document.createElement("script");
    //   s.type = "text/javascript";
    //   s.src = "http://code.jivosite.com/widget/wGPM2QDpTj";
    //   document.head.appendChild(s);
    // }, 5000);

    setTimeout(() => {
      if (window.location.hash) {
        console.log(window.location.hash.split("#")[1]);
        let el = document.getElementById(window.location.hash.split("#")[1]);

        console.log(el);
        if (!el) return;

        el.scrollIntoView({
          behavior: "smooth",
        });
      }
    }, 500);
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
<svelte:head>
  <title>Armada Full Mouth Dental Implant</title>
  <meta name="description" content="Armada Smile Full Mouth Dental Implant" />
</svelte:head>
<main>
  <Navbar />

  <Router primary={false}>
    <Route path="policy" component={Policy}><Policy /></Route>
    {#if isMobile}
      <Route path="/*">
        <Mobile />
      </Route>
    {:else}
      <Route path="/*">
        <Web />
      </Route>
    {/if}
  </Router>
  <Footer />
</main>
