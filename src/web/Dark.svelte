<script>
  import AniButton from "../components/AniButton.svelte";

  import { region } from "../services/store";
  import SmallForm from "./SmallForm.svelte";
  let name;
  let phone;
  let formStatus;
  let warn;
  let country= $region=="uk"?"England":"USA"

  const addRes = async () => {
    let date = new Date().toLocaleString("tr-TR")

    let bodyData = {
      name,
      phone,
      country,
      date

    };
    if (!name || !phone) {
      warn = true;
      return;
    }
    warn = false;
    formStatus = true;
    gtag("event", "conversion", {
      send_to: "AW-10923673526/LRSSCPLmnsIDELaP6Ngo",
    });
    window.dataLayer.push({
      event: "registrationComplete",
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

<section id="dark" class="mt-5  video-bg">
  <div class="container text-center">
    <div class="row">
      <div class="col-12 col-md-7 video-left">
        <div class="">
          <div class="video-left-area">
            <div class="video-left-text pl-5">
              <h2 class="video-header">
                Get information for more favorable packages in implant
                treatments
              </h2>
              <p class="d-none d-xl-block">
                Dental Implants are very expensive especially in {country}
                compared to dental implants in Turkey. But, why would you spend
                a fortune when you can get the same dental products at much more
                affordable prices without compromising the quality? At Armada
                Smile Turkey, we only offer high-end, certified dental implant
                brands with the highest success rates for our patients
              </p>
            </div>
          </div>
        </div>
        <div class="dark-button pl-5">
          <AniButton />
        </div>
      </div>
      <div class="col-12 col-md-5">
  <SmallForm></SmallForm>
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
    height: 315px;
    padding-left: 0px;
    padding-right: 0px;
    color: #fff;
    text-shadow: 0.5px 0.5px black;
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
  
  .contact-form{
    padding: 20px 30px 30px 30px;
    border-radius: 15px;
    background: #fff;
    box-shadow: 0 16px 37px -22px rgba(2, 2, 2, 0.32);
    box-shadow: 0 3px 14px -1px rgba(0, 0, 0, 0.2);
    width: 300px;
    min-height: 317px;
    margin: 0 auto;
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
  
  .free-quote-button {
    background: #ffe91e;
    border-radius: 10px;
    color: #24303d !important;
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
  .dark-button {
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
  }
</style>
