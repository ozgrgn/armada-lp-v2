<script>
  // import AniButton from "../components/AniButton.svelte";
  import LP_JSON from "../assets/lp.json";
  import { region } from "../services/store";
  console.log($region);
  let name;
  let phone;
  let formStatus;
  let warn;
  let country= $region=="uk"?"İngiltere":"Amerika"

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
    style="background: url(/assets/images/hero-3.webp)  no-repeat right center ;background-size: cover; "
  >
    <div class="container">
      <div class="row s ">
        <div class="col-12">
          <div class="hero-banner-content">
            <h1 class="header ">
              <span class="spot">Full Mouth Dental Implants</span>
              <!-- you'll see dynamic css change at below  
                class="d-flex {LP_JSON[$region][
                  'hero-banner-content.strong.css'
                ]}"-->
              <strong
                >{LP_JSON[$region]["hero-banner-content.strong1"]} <br /> {LP_JSON[$region]["hero-banner-content.strong2"]} </strong
              >
            </h1>
            <ul>
              <li>
                <p class="mb-1">
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
            <div class="row tab-button mar-left">
              {#await import("../components/AniButton.svelte") then component}
                <svelte:component this={component.default} />
              {/await}
              <!-- <AniButton /> -->
            </div>
          </div>
        </div>
        <div class="col-12">
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
                    <button
                      type="button"
                      class="free-quote-button"
                      on:click={addRes}
                    >
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
  </div>
</section>

<style>
  button:disabled,
  .mar-left {
    margin-left: 0px !important;
  }
  .banner {
    height: 550px;
    width: 100vw;
    color: white;
    display: flex;
    justify-content: center;
    /* background: linear-gradient(to top, #0c68ec, #4d5369); */
  }
  .header {
    font-size: 1.9rem;
    line-height: 1.3;
    padding-top: 50px;
    margin-bottom: 0;
  }
  .hero-banner-content {
    float: left;
    color: #4d5369;
  }
  .spot {
    color: #4d5369;
    font-size: 20px;
    margin: 0 0 6px 0;
    line-height: 1.2 !important;
  }
  .hero-banner-content h1 span {
    font-weight: 300;
    display: block;
    color: #4d5369;
  }
  p span {
    color: #ba4e5b;
    font-weight: 700;
    font-size: 16px;
  }
  .hero-second-banner {
    line-height: 1.5;
  }

  .hero-contact-form {
    margin-top: 130px;
  }
  .contact-form {
    padding: 20px 30px 30px 30px;
    border-radius: 15px;
    background: #fff;
    box-shadow: 0 16px 37px -22px rgba(2, 2, 2, 0.32);
    box-shadow: 0 3px 14px -1px rgba(0, 0, 0, 0.2);
    width: 300px;
    margin: 0 auto;
  }

  .contact-form p {
    line-height: 1.5;
    font-size: 17px;
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

  .tab-button {
    display: flex;
    flex-direction: column;
  }
</style>
