<script>
  import { link } from "svelte-navigator";

</script>

<a
  class="ani-button" 
  id="wp"
  use:link
  href="https://api.whatsapp.com/send?phone=+905452451254&text=Hello,%0a  I would like to get information about dental Implants."
  target="_blank"
>
  <span />
  <span />
  <span />
  <span />
  <span class="wp"> Whatsapp </span>
  <img src="/assets/images/icons/whatsapp.png" alt="" /> <br /> Get Immediate
  Info
</a>

<style>
  .ani-button {
    cursor: pointer;
    position: absolute;
    text-align: center;
    color: #fff;
    background-color: #ba4e5b;
    padding: 10px 30px;
    font-size: 12px;
    font-weight: 400;
    letter-spacing: 2px;
    text-decoration: none;
    box-shadow: 0 20px 50px rgba(41, 32, 32, 0);
    overflow: hidden;
    border-radius: 10px;
    z-index: 9999999;
  }
  @media only screen and (max-width: 600px) {
    /* .ani-button {
      padding: 5px 10px;
    } */
  }

  .ani-button img {
    vertical-align: text-top;
  }
  .wp {
    padding-top: 7px;
    font-size: 15px !important;
    line-height: 16px;
    font-weight: 700 !important;
    margin: 0 !important;
  }

  .ani-button:before {
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
    background: linear-gradient(to right, rgb(255, 255, 255), #ba4e5b);
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
    background: linear-gradient(to bottom, rgb(255, 255, 255), #ba4e5b);
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
    background: linear-gradient(to left, rgb(255, 255, 255), #ba4e5b);
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
    background: linear-gradient(to top, rgb(255, 255, 255), #ba4e5b);
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
