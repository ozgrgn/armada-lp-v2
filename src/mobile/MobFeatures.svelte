<script>
    import LP_JSON from "../assets/lp.json";
  import { perma } from "../services/store";
  import MobClinic from "./MobClinic.svelte";
</script>

<section id="features">
  <div class="container mb-5">
    <div class="rows">
      <div class="sec-mod-text">
        <div class="">
          <h2 class="tab-header title pb-1">
            {LP_JSON[$perma]["features_title1"]}  {LP_JSON[$perma]["features_title2"]}
          </h2>
          <div class=" ">
            <table class="second-items">
              <tr>
                <td class="sec-img">
                  <img
                    src="/assets/images/icons/dentist.png"
                    alt="dentist"
                    loading="lazy"
                  />
                </td>
                <td>{LP_JSON[$perma]["features1_1"]}  {LP_JSON[$perma]["features1_2"]} </td>
              </tr>
              <tr>
                <td>
                  <img
                    src="/assets/images/icons/{LP_JSON[$perma]["features2_icon"]}.png"
                    alt="implant"
                    loading="lazy"
                  />
                </td>
                <td>{LP_JSON[$perma]["features2_1"]}  {LP_JSON[$perma]["features2_2"]}</td>
              </tr><tr>
                <td>
                  <img
                    src="/assets/images/icons/discount70.png"
                    alt="implant price"
                    loading="lazy"
                  />
                </td>
                <td>{LP_JSON[$perma]["features3_1"]}  {LP_JSON[$perma]["features3_2"]}</td>
              </tr>
              <tr>
                <td>
                  <img
                    src="/assets/images/icons/once_7_days.png"
                    alt="once 7 days"
                    loading="lazy"
                  />
                </td>
                <td>{LP_JSON[$perma]["features4_1"]}  {LP_JSON[$perma]["features4_2"]}</td>
              </tr>
              <tr>
                <td>
                  <img
                    src="/assets/images/icons/hotel-sign.png"
                    alt="hotel"
                    loading="lazy"
                  />
                </td>
                <td>{LP_JSON[$perma]["features5_1"]}  {LP_JSON[$perma]["features5_2"]}</td>
              </tr>
              <tr>
                <td>
                  <img
                    src="/assets/images/icons/info.png"
                    alt="once 7 days"
                    loading="lazy"
                  />
                </td>
                <td>{LP_JSON[$perma]["features6_1"]}  {LP_JSON[$perma]["features6_2"]}</td>
              </tr>
              <tr>
                <td>
                  <img
                    src="/assets/images/icons/check.png"
                    alt="once 7 days"
                    loading="lazy"
                  />
                </td>
                <td>{LP_JSON[$perma]["features7_1"]}  {LP_JSON[$perma]["features7_2"]}</td>
              </tr>
              <tr>
                <td>
                  <img
                    src="/assets/images/icons/language.png"
                    alt="once 7 days"
                    loading="lazy"
                  />
                </td>
                <td>{LP_JSON[$perma]["features8_1"]}  {LP_JSON[$perma]["features8_2"]}</td>
              </tr>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="clinic-3d">
<MobClinic /></div>
</section>

<style>
.clinic-3d {
  padding:15px
}
  .container {
    padding: 0;
  }
  .sec-mod-text {
    margin: 50px 15px 15px 20px;
  }
  table td {
    font-size: 18px;
    line-height: 1.2;
    height: 55px;
  }
  table td img {
    width: 38px;
  }
  .sec-img {
    width: 50px;
  }
  .title {
    color: #24303d !important;
   
  }

  h2 {
    text-align: text;
    padding-left: 5px;
    padding-right: 5px;
    font-size: 4.5vw;
    line-height: 1.4;
  }
</style>
