<script>
  import { link } from "svelte-navigator";
  import { perma } from "../services/store";
  import LP_JSON from "../assets/lp.json";



</script>
{#if $perma}
<section class="top">
  <div class="footer mt-4">
    <div class="container">
      <div class="row">
        <div class="col-md-4 col-12 text-center">
          <img src="/assets/images/icons/location.png" alt="" loading="lazy"/>

          <h5>Contact us</h5>

          <p>Muratpaşa / Antalya / TURKEY</p>

          <p>
            <a href="mailto:info@armadasmile.com">info@armadasmile.com</a>
          </p>
          <a href="tel:{LP_JSON[$perma]["tel"]}">
          <p>{LP_JSON[$perma]["tel"]}
          </p>
        </a>
        </div>
        <div class="col-md-4 col-12 text-center">
          <img src="/assets/images/icons/social-media.png" alt="" loading="lazy"/>

          <h5>Social Media</h5>
          <p>Learn more about us</p>

          <div class="footer-icons mt-3 pt-1 ">
            <a use:link href="tel:+905452451254"><img
              class="ml-1"
              src="/assets/images/icons/phone.webp"
              height="30"
              alt="armada"
              loading="lazy"
            /></a> 
            <a use:link href="https://www.facebook.com/Armada-Smile-653493654802568" target="_blank">
            <img
              class="ml-1"
              src="/assets/images/icons/facebook2.png "
              height="30"
              alt="armada"
              loading="lazy"
            /></a>
            <a use:link href="https://www.instagram.com/armada_smile/" target="_blank"> 
            <img
              class="ml-1"
              src="/assets/images/icons/instagram2.png"
              height="30"
              alt="armada"
              loading="lazy"
            /></a> 

            <a href="https://api.whatsapp.com/send?phone=+905452451254&text=Hello,%0a  I would like to get information about dental Implants.">
            <img
              class="ml-1"
              src="/assets/images/icons/whatsappthin.png"
              height="30"
              alt="armada"
              loading="lazy"
            /></a>
          </div>
        </div>
        <div class="col-md-4 col-12 text-center pt-2">
          <img src="/assets/images/icons/link.png" alt=""  loading="lazy"/>

          <h5>Service Policy</h5>
          <p>We give importance to your privacy</p>

          <a use:link href="./policy"> Our cookie policy</a> <br />
          <a use:link href="/"> Privacy terms</a>
        </div>
      </div>
    </div>
  </div>

  <div class="container-fluid footer-bottom px-0">
    <!--begin row -->

    <div class="row no-gutters mx-0">
      <!--begin col-md-12 -->

      <div class="col-md-12 text-center">
        <p>
          Copyright © 2022 Armada Smile
        </p>
      </div>

      <!--end col-md-6 -->
    </div>

    <!--end row -->
  </div>
</section>
{/if}
<style>
    @media only screen and (min-width: 600px) {
      .top{
    margin-top:50px !important;
  }
}
  .top{
    margin-top:250px
  }
    .footer-bottom {
    background-color: #fff;
    height: 60px;
  }
  .footer p {
    margin-top: -7px;
    color: #141414;
    margin-bottom: 10 px;
    line-height: 1.43;
  }
</style>