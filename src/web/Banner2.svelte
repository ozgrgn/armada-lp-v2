<script>
  import AniButton from "../components/AniButton.svelte";
  import Carousel from "svelte-carousel";
  import LP_JSON from "../assets/lp.json";

  import { region } from "../services/store";
 
  let name;
  let phone;
  let formStatus;
  let warn;
  let country= $region=="uk"?"İngiltere":"Amerika"



  const addRes = async () => {
    let bodyData = {
      name,
      phone,
      country,
    };
    if (!name || !phone) {
      warn = true;
      return;
    }
    warn = false;
    formStatus = true;
    console.log(bodyData,"bodydata bannerdan")

    gtag("event", "conversion", {
      send_to: "AW-10923673526/LRSSCPLmnsIDELaP6Ngo",
    });

    window.dataLayer.push({
      event: "registrationComplete",
      "custom.gtm.element": "register",
    });

    const res = await fetch("https://armada-lp-backend.herokuapp.com", {
      // const res = await fetch("http://localhost:3000", {
      method: "POST",
      body: JSON.stringify(bodyData),
      headers: {
        "content-type": "application/json",
      },
    });

    const json = await res.json();
    console.log(json);
  };
</script>

<section id="header">
  <div
    class="banner"
    style="background: url(../../assets/images/hero-3.png)  no-repeat right center ;background-size: cover; "
  >
    <div class="container">
      <div class="row  ">
        <div class="col-7 d-flex justify-content-center ">
          <div class="right-area">
            <div class="hero-banner-content">
              <h1 class="header">
                <span class="spot">Full Mouth Dental Implants</span>

                <strong>{LP_JSON[$region]["hero-banner-content.strong1"]} <br /> {LP_JSON[$region]["hero-banner-content.strong2"]} </strong
                >
              </h1>
             
              <ul>
                <li> <p class='mb-1'>
                  <span>70% Less</span> price than abroad
                   </p>
                </li>
              </ul>  
             <ul>
               <li>
                <p class="hero-second-banner mt-0">
                  Full mouth dental implants with crown <br />is completed in
                  <span>just 7 days</span>
                </p>
               </li>
             </ul>
             
              <div class="row ani-button-area m-0">
                <AniButton/>
              </div>
            </div>
          </div>
        </div>
        <div class="col-5">
          <div class="hero-contact-form">
            <div class=" contact-form">
              <p>Diagnosis And Cost In Minutes</p>
              <form class="contact__form">
                <div
                  class="alert alert-success contact__msg {formStatus == true
                    ? 'display'
                    : 'no-display'}"
                  role="alert"
                >
                  Your message was sent successfully.
                </div>
                <div
                class="alert-warn  contact__msg {warn == true
                  ? 'display'
                  : 'no-display'}"
                role="alert"
              >
                Please enter your name and phone
              </div>
                <ul class={formStatus == true ? "no-display" : "display"}>
                  <li style=" height:50px !important;">
                    <input
                      style="
                        background: url('/assets/images/icons/user.png') no-repeat
                          scroll 7px 11px;
                        background-size: 20px 20px;
                        padding-left: 35px; 
                       
                      "
                      type="text"
                      name="name"
                      placeholder="Name Surname"
                      autocomplete="name"
                      bind:value={name}
                    />
                    />
                  </li>
                  <li>
                    <input
                      style="
                        background: url('/assets/images/icons/{$region}.png') no-repeat
                          scroll 7px 11px;
                        background-size: 20px 20px;
                        padding-left: 35px;
                      "
                      type="tel"
                      name="tel"
                      placeholder="Phone"
                      autocomplete="tel"
                      bind:value={phone}
                    />
                  </li>
                  <li>
                    <button
                      type="button"
                      class="free-quote-button"
                      on:click={addRes}
                    >
                      Get Free Quote</button
                    >
                    <!-- <input
                      type="submit"
                      obc
                      name="submit"
                      value="Get Free Quote"
                    /> -->
                  </li>
                  <li />
                </ul>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- REVIEWS -->
  <div class="box hidden-xs">
    <div class="container">
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
    color: #4d5369;
    margin: 0;
    font-size: 46px;
    line-height: 50px;
    font-weight: 500;
    text-shadow: 0.5px 0.5px black;
  }
  .title {
    color: #4d5369 !important;
    text-shadow: none;
  }
  /* BANNER */
  .banner {
    height: 600px;
    width: 100vw;
    color: white;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding-top: 120px;
    /* background: linear-gradient(to top, #0c68ec, #4d5369); */

    background-repeat: no-repeat;
    background-size: cover;
  }
  .hero-banner-content {
    color: #4d5369;
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
    color: #4d5369;
    font-size: 33px;
    margin: 0 0 6px 0;
    line-height: initial;
    text-shadow: 0.5px 0.5px black;
  }
  .hero-banner-content h1 span {
    font-weight: 300;
    display: block;
    color: #4d5369;
    text-shadow: 0.5px 0.5px black;
  }
  .hero-contact-form {
    text-align: -webkit-center;
  }
  .contact-form {
    height: 326px;
    padding: 20px 30px 30px 30px;
    border-radius: 15px;
    background: #fff;
    box-shadow: 0 16px 37px -22px rgba(2, 2, 2, 0.32);
    box-shadow: 0 3px 14px -1px rgba(0, 0, 0, 0.2);
    width: 300px;
  }

  .contact-form p {
    line-height: 1.5;

    font-size: 21px;
    text-align: center;
    font-weight: 700;
    margin-bottom: 18px;
    color: #273c56;
  }

  .contact-form form {
    width: 100%;
    box-sizing: border-box;
  }
  .alert-success {
    color: #155724;
    background-color: #d4edda;
    border-color: #c3e6cb;
    text-align: center;
  }
  .alert {
    position: relative;
    padding: 0.75rem 1.25rem;
    margin-bottom: 1rem;
    border: 1px solid transparent;
    border-radius: 0.25rem;
  }
  .alert-warn {
    position: relative;
    color: grey;
    font-size: 12px;
  }
  .contact-form form ul li input,
  .free-quote-button {
    width: 100%;
    margin-top: 10px;
    display: block;
    line-height: 29px;
    font-size: 14px;
    outline: none;
    height: 45px;
    background: #ffffff;
    padding-left: 45px;
    box-sizing: border-box;
    border-radius: 10px;
    color: #1a2a38;
    border: 1px solid #e4e4e4;
    background: #f5f5f5;
    box-shadow: 2px 2px 3px #bfbfbf4d;
  }
  .banner form ul li p {
    margin-bottom: 0px;
    color: #6a6a6a;
    font-size: 12px;
    text-align: center;
  }
  .free-quote-button {
    background: #ba4e5b;
    border-radius: 10px;
    color: #fff;
    height: 50px;
    line-height: 50px;
    font-weight: 600;
    font-size: 16px;
    text-align: center;
    cursor: pointer;
    padding-left: 0;
    text-transform: capitalize;
  }
  .small-form form ul li input {
    height: 35px;
    border-radius: 5px;
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
</style>
