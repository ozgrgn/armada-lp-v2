<script>
  import { link } from "svelte-navigator";
  import LP_JSON from "../assets/lp.json";
  import { perma } from "../services/store";

</script>

<a
  class="ani-button" 
  id="wp"
  use:link
  href="https://api.whatsapp.com/send?phone= {LP_JSON[$perma]["wp"]} &text=Hello,%0a  {LP_JSON[$perma]["wp_message"]}"
  target="_blank"
>
  <span />
  <span />
  <span />
  <span />
  <span class="wp"> Whatsapp </span>
  <img class="icon" src="/assets/images/icons/whatsapp-sm.png" alt="" /> <br /> <p class="p-0 m-0 get-info">Get Immediate
  Info</p>
</a>

<style>
.icon {
  height: 16px;
}
.get-info {
  font-weight: 500;
}
.ani-button {
    cursor: pointer;
    position: absolute;
    text-align: center;
    color: #24303d !important;
    background-color: #ffe91e;
    padding: 10px 30px;
    font-size: 12px;
    font-weight: 400;
    letter-spacing: 2px;
    text-decoration: none;
    box-shadow: 0 20px 50px rgba(41, 32, 32, 0);
    overflow: hidden;
    border-radius: 10px;
    z-index: 999;
  }

  .ani-button img {
    vertical-align: text-top;
  }
  .wp {
    padding-top: 7px;
    font-size: 16px !important;
    line-height: 16px;
    font-weight: 700 !important;
    margin: 0 !important;
  }  .ani-button:before {
    position: absolute;
    top: 2px;
    left: 2px;
    bottom: 2px;
    content: "";
    width: 50%;
  }

  .ani-button span:nth-child(1) {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 2px;
    background: linear-gradient(to right, rgb(255, 255, 255), #ffe91e);
    animation: animate1 2s linear infinite;
  }

  @keyframes animate1 {
    0% {
      transform: translateX(-100%);
    }

    100% {
      transform: translateX(100%);
    }
  }

  .ani-button span:nth-child(2) {
    position: absolute;
    top: 0;
    right: 0;
    width: 2px;
    height: 100%;
    background: linear-gradient(to bottom, rgb(255, 255, 255), #ffe91e);
    animation: animate2 2s linear infinite;
    animation-delay: 1s;
  }

  @keyframes animate2 {
    0% {
      transform: translateY(-100%);
    }

    100% {
      transform: translateY(100%);
    }
  }

  .ani-button span:nth-child(3) {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 2px;
    background: linear-gradient(to left, rgb(255, 255, 255), #ffe91e);
    animation: animate3 2s linear infinite;
  }

  @keyframes animate3 {
    0% {
      transform: translateX(100%);
    }

    100% {
      transform: translateX(-100%);
    }
  }

  .ani-button span:nth-child(4) {
    position: absolute;
    top: 0;
    left: 0;
    width: 2px;
    height: 100%;
    background: linear-gradient(to top, rgb(255, 255, 255), #ffe91e);
    animation: animate4 2s linear infinite;
    animation-delay: 1s;
  }

  @keyframes animate4 {
    0% {
      transform: translateY(100%);
    }

    100% {
      transform: translateY(-100%);
    }
  }
</style>
