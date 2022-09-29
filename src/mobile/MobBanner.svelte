<script>
  // import AniButton from "../components/AniButton.svelte";
  import LP_JSON from "../assets/lp.json";
  import { region } from "../services/store";
  import AniButton from "../components/AniButton.svelte";
  import MobSmallForm from "./MobSmallForm.svelte";
  console.log($region);
  let name;
  let phone;
  let email;
  let formStatus;
  let warn;
  let country = $region == "uk" ? "England" : "USA";

  const addRes = async () => {
    let date = new Date().toLocaleString("tr-TR");

    let bodyData = {
      name,
      phone,
      country,
      date,
      email
    };
    if (!name || !phone) {
      warn = true;
      return;
    }
    warn = false;
    formStatus = true;
    console.log(bodyData, "bodydata");

    window.dataLayer.push({
      event: "registrationComplete",
    });

    window.dataLayer.push({
      event: "registrationComplete",
      "custom.gtm.element": "register",
    });
    // https://armada-lp-backend.herokuapp.com
    const res = await fetch("https://armada-lp-backend.herokuapp.com", {
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
    style="background: url(/assets/images/hero.jpeg)  no-repeat center center ;background-size: cover; "
  >
  <div class="overlay" />
    <div class="container oil">
      <div class="row s ">
        <div class="col-12">
          <div class="hero-banner-content">
            <h1 class="header spot ">
              Full Mouth Dental Implants</h1>
              <!-- you'll see dynamic css change at below  
                class="d-flex {LP_JSON[$region][
                  'hero-banner-content.strong.css'
                ]}"-->
              <h3
                >{LP_JSON[$region]["hero-banner-content.strong1"]} 
                {LP_JSON[$region]["hero-banner-content.strong2"]}
                </h3>
           
            <ul>
              <li>
                <p class="mb-1">
                  Implant prices starting from <span>499$</span>
                </p>
              </li>
            </ul>
            <ul>
              <li>
                <p class="hero-second-banner mt-0">
                  Full mouth dental implants with crown is completed in
                  <span>just 7 days</span>
                </p>
              </li>
            </ul>
            <div class="tab-button mar-left">
              <div class="button-container">
              <AniButton />
        
            </div>
              <!-- <AniButton /> -->
            </div>
          </div>
        </div>
        <div class="col-12 space">
       <MobSmallForm>
       </MobSmallForm>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
 
  .banner {
    position: relative;
    height: 550px;
    width: 100vw;
    color: white;
    display: flex;
    justify-content: center;
    /* background: linear-gradient(to top, #0c68ec, #ffffff); */
  }
  .header {
    font-size: 1.9rem;
    line-height: 1.3;
    padding-top: 50px;
    margin-bottom: 0;
  }
  .hero-banner-content {
    text-shadow: 0.5px 0.5px black;
    float: left;
    color: #ffffff;
  }
  .spot {
    color: #ffffff;
    font-size: 6.5vw;
    margin: 0 0 6px 0;
    line-height: 0.5; 
    text-shadow: 0.5px 0.5px black;
  }

  .hero-banner-content h1 span {
    font-weight: 300;
    display: block;
    color: #ffffff;
  }
  h3 {
    font-size: 6.5vw;
    margin: 0;
  }
  p {
    font-weight: 700;
    font-size: 18px;
  }
  p span {
    color: #ffe91e;
    font-weight: 700;
    font-size: 18px;
  }
  .hero-second-banner {
    line-height: 1.5;
  }

  .button-container {
    height: 110px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-shadow: none;
  }
  .tab-button {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .space {
    margin-top:30px
  }
  .overlay {
    position: absolute;
    left: 0;
    top: 0;
    z-index: 1;
    background: rgb(0, 0, 0);
    background: rgba(0, 0, 0, 0.5); /* Black see-through */
    width: 100%;
    height: 100%;
  }
  .oil {
    z-index: 10;
  }
</style>
