<script>
      import AniButton from "../components/AniButton.svelte";
      import LP_JSON from "../assets/lp.json";
  import { perma } from "../services/store";
</script>


<section id="features" class=" mx-5 ">
    <div class="container cont-75 my-5 py-4">
      <div class="row   " >
        <div class="col-6 tab-container-left ">
          <div class="">
            <h2 class="tab-header title pt-2">
              {LP_JSON[$perma]["features_title1"]}<br /> {LP_JSON[$perma]["features_title2"]}
            </h2>
            <div class="d-none d-xl-block ">
              <table class="second-items">
                <tr>
                  <td>
                    <img src="/assets/images/icons/dentist.png" alt="dentist" />
                  </td>
  
                  <td>{LP_JSON[$perma]["features1_1"]} <br /> {LP_JSON[$perma]["features1_2"]} </td>
                  <td>
                    <img src="/assets/images/icons/implant.png" alt="implant" />
                  </td>
                  <td>{LP_JSON[$perma]["features2_1"]} <br /> {LP_JSON[$perma]["features2_2"]}</td>
                </tr>
                <tr>
                  <td>
                    <img
                      src="/assets/images/icons/discount70.png"
                      alt="implant price"
                    />
                  </td>
                  <td>{LP_JSON[$perma]["features3_1"]} <br /> {LP_JSON[$perma]["features3_2"]}</td>
                  <td>
                    <img
                      src="/assets/images/icons/once_7_days.png"
                      alt="once 7 days"
                    />
                  </td>
                  <td>{LP_JSON[$perma]["features4_1"]} <br /> {LP_JSON[$perma]["features4_2"]}</td>
                </tr>
  
                <tr>
                  <td>
                    <img src="/assets/images/icons/hotel-sign.png" alt="hotel" />
                  </td>
                  <td>{LP_JSON[$perma]["features5_1"]} <br /> {LP_JSON[$perma]["features5_2"]}</td>
                  <td>
                    <img src="/assets/images/icons/info.png" alt="once 7 days" />
                  </td>
                  <td>{LP_JSON[$perma]["features6_1"]} <br /> {LP_JSON[$perma]["features6_2"]}</td>
                </tr>
  
                <tr>
                  <td>
                    <img src="/assets/images/icons/check.png" alt="check" />
                  </td>
                  <td>{LP_JSON[$perma]["features7_1"]} <br /> {LP_JSON[$perma]["features7_2"]}</td>
                  <td>
                    <img
                      src="/assets/images/icons/language.png"
                      alt="implant treatment info"
                    />
                  </td>
                  <td>{LP_JSON[$perma]["features8_1"]} <br /> {LP_JSON[$perma]["features2_2"]}</td>
                </tr>
              </table>
            </div>
          </div>
          <div class="tab-button">
            <AniButton />
          </div>
        </div>
        <div class="col-6 tab-container-right pt-3">
          <!-- <div class="row justify-content-center">
          <h3 class="title mt-2">Implant Structure</h3></div> -->
          <img src="/assets/images/a.jpeg" class="image" alt="" />
        </div>
      </div>
    </div>
  </section>


  <style>

  .second-items td {
    height: 70px;
    line-height: 1.4;
    font-size: 1.2vw;
    font-weight: 600;
    color: #24303d;
  }
  .tab-container-left {
    padding-left: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .tab-container-right {
    text-align: right;
  }
  .tab-container-right img {
    width: 86%;
    box-shadow: 5px 5px 10px 0 rgb(97 97 97 / 70%);
    border-radius: 10px;
  }
  .tab-header {
    margin-top: 0;
    margin-bottom: 15px;
    line-height: 2rem;
    color:#24303d !important;
  
  }
  h2 {
    font-size:1.7vw !important
  }

  .tab-button {
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
  }
  </style>