<script>

import { link } from "svelte-navigator";

function scrollIntoView({ target }) {
		const el = document.querySelector(target.getAttribute('href'));   
     console.log(el)
		if (!el) return;

    el.scrollIntoView({
      behavior: 'smooth'
    });
  }
   
</script>

<!-- NAVBAR -->
<nav
  id="navbar-main"
  class="navbar sticky-top navbar-light navbar-expand-lg headroom headroom--top headroom--pinned"
>
  <div class="container-fluid">
    <div class="row bar">
      <div class="navbar-brand">
        <a class="navbar-brand" use:link href="/"
          ><img
            class="navbar-brand  pl-3 mt-2"
            src="/assets/images/logos/armada-smile-logo.png"
            height="50"
            alt="armada"
          /></a
        >
      </div>
      <div class="navbar-icons mt-3 mr-2  ">
      <a use:link href="tel:+905452451254"> <img
          class="ml-1"
          src="/assets/images/icons/phone-call.png"
          height="30"
          alt="armada"
       
        /></a> 
        <a use:link href="https://www.facebook.com/Armada-Smile-653493654802568" target="_blank">  <img
          class="ml-1"
          src="/assets/images/icons/facebook.png"
          height="30"
          alt="armada"
        /></a> 
        <a use:link href="https://www.instagram.com/armada_smile/" target="_blank"> <img
          class="ml-1"
          src="/assets/images/icons/instagram.png"
          height="30"
          alt="armada"
        /></a> 
        <a use:link href="https://api.whatsapp.com/send?phone=+905452451254&text=Hello,%0a  I would like to get information about dental Implants."target="_blank">
        <img
          class="ml-1"
          src="/assets/images/icons/whatsapp3.png"
          height="30"
          alt="armada"
        /></a>
      </div>
    </div>
  </div>
</nav>

<style>
      #navbar-main {
    background: #ba4e5b !important;
    box-shadow: 0 16px 37px -22px rgba(2, 2, 2, 0.32);
  }
  .bar {
    background: #ba4e5b !important;
    height: 65px;
    display: flex;
    justify-content: space-between;
  }
  @media only screen and (min-width: 600px) {
  .navbar-brand {
    margin-left:0.5rem
  }
  .navbar-icons {
    margin-right: 2.5rem !important;
  }
}
</style>