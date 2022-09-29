<script>
  import AniButton from "../components/AniButton.svelte";
  import LP_JSON from "../assets/lp.json";
  import { perma } from "../services/store";
  import { region } from "../services/store";
  import MobSmallForm from "./MobSmallForm.svelte";
  let country = $region == "uk" ? "England" : "USA";
</script>

<section id="dark" class="video-bg  mt-4">
  <div class="container">
    <div class="rows">
      <div class="video-left">
        <div class="video-left-text">
          <h2 class="video-header">
            Get information for more advantageous packages in <span>
              {LP_JSON[$perma][
                "treatment"
              ]} treatments
            </span>
          </h2>
          <p class="">
            Dental {LP_JSON[$perma]["treatment"]} treatments are very expensive especially
            in {country}
            compared to dental {LP_JSON[$perma]["treatment"]} treatments in Turkey.
            But, why would you spend a fortune when you can get the same dental products
            at much more affordable prices without compromising the quality? At Armada
            Smile Turkey, we only offer high-end, certified dental {LP_JSON[
              $perma
            ]["treatment"]}
            brands with the highest success rates for our patients
          </p>
        </div>
        <div class="tab-button">
          <AniButton />
        </div>
      </div>

      <div class="col-12 p-0 col-md-6 video-right">
        <MobSmallForm />
      </div>
    </div>
  </div>
</section>

<style>
  .video-bg {
    background-color: #24303d;
    height: 700px;
  }

  .video-left {
    padding: 45px 5px 5px;
    color: #fff;
  }
  .video-left-text {
    text-align: justify;
  }
  .video-left p {
    font-size: 14px;
  }
  .video-header {
    text-align: left;
    color: #ffffff;
    font-size: 26px;
    line-height: 38px;
    font-weight: 500;
    margin-bottom: 18px;
    margin-top: 0;
  }
  .video-right {
    padding-top: 100px !important;
  }

  .tab-button {
    padding-top: 20px;
  }
</style>
