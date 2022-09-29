<script>
  import AniButton from "../components/AniButton.svelte";
  import Carousel from "svelte-carousel";
  import LP_JSON from "../assets/lp.json";
  import { perma } from "../services/store";
  import SmallForm from "./SmallForm.svelte";

  console.log($perma);
</script>

<section id="header">
  <div
    class="banner"
    style="background: url(../../assets/images/hero.jpeg)  no-repeat right center ;background-size: cover; "
  >
    <div class="overlay" />
    <div class="container oil">
      <div class="row">
        <div class="col-7 d-flex justify-content-center ">
          <div class="right-area">
            <div class="hero-banner-content  ">
              <div class="d">
                <h1 class="header spot">{LP_JSON[$perma]["banner_h1"]}</h1>
                <h3>
                  {LP_JSON[$perma]["hero-banner-content.strong1"]}
                  <span>
                    {LP_JSON[$perma]["hero-banner-content.strong2"]}
                  </span>
                </h3>

                <ul class="my-4">
                  <li>
                    <p class="mb-1">
                      {LP_JSON[$perma]["hero-banner-content.second1"]}
                      <span
                        >{LP_JSON[$perma]["hero-banner-content.second2"]}
                      </span>
                    </p>
                  </li>

                  <li>
                    <p class="hero-second-banner mt-0">
                      {LP_JSON[$perma]["hero-banner-content.third1"]}<br />
                      {LP_JSON[$perma]["hero-banner-content.third2"]}
                      <span>  {LP_JSON[$perma]["hero-banner-content.third3"]}</span>
                    </p>
                  </li>
                </ul>
              </div>
              <div class="button-container">
                <AniButton />
              </div>
            </div>
          </div>
        </div>
        <div class="col-5">
          <SmallForm />
        </div>
      </div>
    </div>
  </div>

  <!-- REVIEWS -->
  <div class="box hidden-xs">
    <div class="container oil">
      <div class="outerb">
        <!-- Comments -->
        <div class="rows">
          <Carousel particlesToShow={4} particlesToScroll={3} dots={false}>
            <div>
              <div class="review-container">
                <div class="small-image">
                  <img
                    class="small-image"
                    src="/assets/images/clinic/1.png"
                    alt=""
                  />
                </div>
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/2.png"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/3.png"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/4.png"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/5.png"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/6.png"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/7.png"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/8.png"
                  alt=""
                />
              </div>
            </div>
          </Carousel>
          <h3 class="text-center title  mt-0 pb-3">
            Armada Smile Dental - Antalya / Turkey
          </h3>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  /* GENERAL */

  .header {
    color: #ffffff;
    margin: 0;
    font-size: 28px;
    line-height: 30px;
    font-weight: 500;
    text-shadow: 0.5px 0.5px black;
  }
  .title {
    color: #24303d !important;
    text-shadow: none;
  }
  /* BANNER */
  .banner {
    position: relative;
    height: 600px;
    width: 100vw;
    color: white;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding-top: 120px;
    /* background: linear-gradient(to top, #0c68ec, #ffffff); */

    background-repeat: no-repeat;
    background-size: cover;
  }
  .right-area {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .hero-banner-content {
    color: #ffffff;
  }

  .hero-banner-content p {
    margin-top: 0.8rem;
    font-size: 22px;
    font-weight: 500;
  }
  .hero-second-banner {
    line-height: 1.3;
  }
  .spot {
    font-size: 40px;
    margin: 0 0 6px 0;
    text-shadow: 0.5px 0.5px black;
    font-weight: 600 !important;
  }
  .hero-banner-content h3 {
    font-size: 35px;
    line-height: 0px;
    text-shadow: 1px 1px black;
  }
  .hero-banner-content h1 span {
    font-weight: 600;
    color: #ffe91e;
    text-shadow: 1px 1px black;
  }
  .button-container {
    height: 70px;
    display: flex;
    flex-direction: column;
    justify-content: end;
  }
  .banner form ul li p {
    margin-bottom: 0px;
    color: #6a6a6a;
    font-size: 12px;
    text-align: center;
  }

  .box {
    margin-top: -70px;
    display: flex;
    justify-content: center;
  }

  .box .outerb {
    min-height: 150px;
    background: #ffffff;
    border-radius: 10px;
    box-shadow: 5px 5px 10px 0 rgba(97, 97, 97, 0.7);
  }
  /* REVIEWS */

  .review-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 10px;
    padding-top: 20px;
  }
  .small-image {
    width: 100%;
  }
  .overlay {
    position: absolute;
    left: 0;
    top: 0;
    z-index: 1;
    background: rgb(0, 0, 0);
    background: rgba(0, 0, 0, 0.3); /* Black see-through */
    width: 100%;
    height: 100%;
  }
  .oil {
    z-index: 10;
  }
</style>
