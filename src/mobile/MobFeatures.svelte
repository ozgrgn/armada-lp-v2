<script>

    import AniButton from "../components/AniButton.svelte";
    
    </script>
  
<section id="features">
    <div class="container">
      <div class="rows   ">
        <div class=" sec-mod-text ">
          <div class="">
            <h2 class="tab-header title pb-3">
              Why should I have <span> Implant treatment</span> at Armada Smile Turkey?
            </h2>
            <div class=" ">
              <table class="second-items">
                <tr>
                  <td class="sec-img">
                    <img src="/assets/images/icons/dentist.png" alt="dentist" loading="lazy"/>
                  </td>
                  <td>Specialists in  implant treatments</td>
                </tr>
                <tr>
                  <td>
                    <img src="/assets/images/icons/implant.png" alt="implant" loading="lazy" />
                  </td>
                  <td> The world’s best  implant brands</td>
                <tr>
                  <td>
                    <img
                      src="/assets/images/icons/discount70.png"
                      alt="implant price" 
                      loading="lazy"
                    />
                  </td>
                  <td>70% more affordable prices</td>
                </tr>
                <tr>
                  <td>
                    <img
                      src="/assets/images/icons/once_7_days.png"
                      alt="once 7 days" 
                      loading="lazy"
                    />
                  </td>
                  <td> Period of treatments  just in 7 days </td>
                </tr>
                <tr>
                  <td>
                    <img src="/assets/images/icons/hotel-sign.png" alt="hotel" loading="lazy" />
                  </td>
                  <td> Free hotel accommodation</td>
                </tr>
                <tr>
                  <td>
                    <img src="/assets/images/icons/info.png" alt="once 7 days" loading="lazy" />
                  </td>
                  <td>Airport-Hotel-Clinic  free transfer </td>
                </tr>
  
             
              </table>
            </div>
          </div>
          <div class="tab-button pt-4 ">
           <AniButton/>
          </div>
        </div>
       
      </div>
    </div>
    <div class="row w-100 p-0 m-0">
    <div class="sec-mod-img p-0 m-0">
      <img src="/assets/images/a.webp" class="image" alt="" loading="lazy" />
    </div></div>
  </section>

  <style>
    .sec-mod-text {
    margin: 50px 15px 15px 15px;
  }
  table td {
    font-size:18px;
    line-height: 1.4;
    height: 60px;
  }
  table td img {
    width: 38px;
  }
  .sec-img {
    width: 50px;
  }
  .title {
    color: #4d5369 !important;
    text-shadow: 0.5px 0.5px 1px rgba(0, 0, 0, 0.20);
  }
  .title span {
    color: #ba4e5b;
  }
  .tab-button {
    display: flex;
    flex-direction: column;
    z-index: 999999999;
  }
  .image {
    width: 100vw;
    margin-top: 100px;
  }
  h2 {
    font-size: 21px;
    line-height: 1.4;
  }
  </style>