<script>
      import AniButton from "../components/AniButton.svelte";
</script>


<section id="features" class=" mx-5 ">
    <div class="container cont-75 my-5 py-4">
      <div class="row   " >
        <div class="col-6 tab-container-left ">
          <div class="">
            <h2 class="tab-header title pt-2">
              Why should I have <span> Implant treatment</span> <br /> at Armada Smile
              Turkey?
            </h2>
            <div class="d-none d-xl-block ">
              <table class="second-items">
                <tr>
                  <td>
                    <img src="/assets/images/icons/dentist.png" alt="dentist" />
                  </td>
  
                  <td>Specialists in <br /> implant treatments</td>
                  <td>
                    <img src="/assets/images/icons/implant.png" alt="implant" />
                  </td>
                  <td> The world’s best <br /> implant brands</td>
                </tr>
                <tr>
                  <td>
                    <img
                      src="/assets/images/icons/discount70.png"
                      alt="implant price"
                    />
                  </td>
                  <td>70% more <br />affordable prices</td>
                  <td>
                    <img
                      src="/assets/images/icons/once_7_days.png"
                      alt="once 7 days"
                    />
                  </td>
                  <td> Period of treatments <br /> just in 7 days </td>
                </tr>
  
                <tr>
                  <td>
                    <img src="/assets/images/icons/hotel-sign.png" alt="hotel" />
                  </td>
                  <td> Free hotel <br />accommodation</td>
                  <td>
                    <img src="/assets/images/icons/info.png" alt="once 7 days" />
                  </td>
                  <td>Airport-Hotel-Clinic <br /> free transfer </td>
                </tr>
  
                <tr>
                  <td>
                    <img src="/assets/images/icons/check.png" alt="check" />
                  </td>
                  <td> Free Consultation <br />& X-rays</td>
                  <td>
                    <img
                      src="/assets/images/icons/language.png"
                      alt="implant treatment info"
                    />
                  </td>
                  <td>English speaking team <br /> in all your appointments</td>
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
    font-size: 18px;
    font-weight: 600;
    color: #4d5369;
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
    line-height: 2.5rem;
  }

  .tab-button {
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
  }
  </style>