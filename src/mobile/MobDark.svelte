<script>
        import AniButton from "../components/AniButton.svelte";
        import { region } from "../services/store";
      let name;
  let phone;
  let formStatus;
  let warn;
  let country= $region=="uk"?"İngiltere":"Amerika"
  console.log(country)

  const addRes = async () => {
    let bodyData = {
      name,
      phone,
      country
    };
    if (!name || !phone) {
      warn = true;
      return;
    }
    warn = false;
    formStatus=true
    console.log(bodyData,"bodydata")
    
    gtag("event", "conversion", {
      send_to: "AW-10923673526/LRSSCPLmnsIDELaP6Ngo",
    });
    window.dataLayer.push({
      event: "registrationComplete",
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
<section id="dark" class="video-bg">
    <div class="container">
      <div class="rows">
        <div class="video-left">
          <div class="video-left-text">
            <h2 class="video-header">
              Get information for more advantageous packages in <span> implant treatments </span>
            </h2>
            <p class="">
              Dental Implants are very expensive especially in England compared
                to dental implants in Turkey. But, why would you spend a fortune
                when you can get the same dental products at much more affordable
                prices without compromising the quality? At Armada Smile Turkey,
                we only offer high-end, certified dental implant brands with the
                highest success rates for our patients
            </p>
          </div>
          <div class="tab-button">
           <AniButton/>
          </div>
        </div>
  
        <div class="col-12 p-0 col-md-6 video-right">
          <div class="hero-contact-form">
            <div class=" contact-form">
              <p>Diagnosis And Cost In Minutes</p>
              <form class="contact__form">
                <div
                  class="alert alert-success contact__msg {formStatus==true ? 'display' : 'no-display'}"
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
                <ul class="{formStatus==true ? 'no-display' : 'display'}">
                  <li>
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
                    <button type="button" class="free-quote-button" on:click={addRes}>
                      Get Free Quote</button
                    >
                  </li>
                  <li />
                </ul>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <style>


  .video-bg {
    background-color: #4d5369;
    height: 700px;
  }


  .video-left {
    padding: 45px 15px 15px;
    color: #fff;
    text-shadow: 0.5px 0.5px black;
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
  .contact-form{
    padding: 20px 30px 30px 30px;
    border-radius: 15px;
    background: #fff;
    box-shadow: 0 16px 37px -22px rgba(2, 2, 2, 0.32);
    box-shadow: 0 3px 14px -1px rgba(0, 0, 0, 0.2);
    width: 300px;
    margin: 0 auto;
  }
  .contact-form p {
    font-size: 16px;
    text-align: center;
    font-weight: 500;
    margin-bottom: 18px;
    color: #273c56;
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
  .contact-form form ul li input, .free-quote-button {
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
  </style>