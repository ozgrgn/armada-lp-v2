<script>
  import AniButton from "../components/AniButton.svelte";
  import LP_JSON from "../assets/lp.json";
  import { perma } from "../services/store";
  import { region } from "../services/store";
  import SmallForm from "./SmallForm.svelte";
  let country = $region == "uk" ? "England" : "USA";
</script>

<section id="dark" class="mt-5  video-bg">
  <div class="container text-center">
    <div class="row">
      <div class="col-12 col-md-7 video-left">
        <div class="">
          <div class="video-left-area">
            <div class="video-left-text pl-5">
              <h2 class="video-header">
                {LP_JSON[$perma]["dark_header"]}
              </h2>
              <p class="d-none d-xl-block">
                {LP_JSON[$perma]["dark_text"]}
              </p>
            </div>
          </div>
        </div>
        <div class="dark-button pl-5">
          <AniButton />
        </div>
      </div>
      <div class="col-12 col-md-5">
        <SmallForm />
      </div>
    </div>
  </div>
</section>

<style>
  .video-bg {
    background-color: #24303d;
    height: 450px;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .video-left {
    height: 294px;
    padding-left: 0px;
    padding-right: 0px;
    color: #fff;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .video-left-text {
    text-align: justify;
  }
  .video-left p {
    font-size: 15px;
  }
  .video-header {
    text-align-last: justify;
    color: #ffffff;
    font-size: 35px;
    line-height: 46px;
    font-weight: 500;
    margin-bottom: 0;
    margin-top: 0;
  }

  .dark-button {
    text-shadow: none;
    position: relative;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }
</style>
