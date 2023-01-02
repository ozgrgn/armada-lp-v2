<script>
  import { region } from "../services/store";
  import { perma } from "../services/store";
  import LP_JSON from "../assets/lp.json";
  let name;
  let phone;
  let email;
  let formStatus;
  let warn;
  let lp = $region +"/"+ $perma
  const addRes = async () => {
    let date = new Date().toLocaleString("tr-TR");

    let bodyData = {
      name,
      phone,
      lp,
      email,
      date,
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
      "custom.gtm.element": "register",
    });

    const res = await fetch("https://super--backend.herokuapp.com/armada-lp", {
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

<div class="hero-contact-form">
  <div class="contact-form">
    <h2 class="form-header">
        {LP_JSON[$perma]["form_title1"]}
      <br> {LP_JSON[$perma]["form_title2"]}
    </h2>
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
        <li style=" height:45px !important;">
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
            <input
            style="
              background: url('/assets/images/icons/email.png') no-repeat
                scroll 7px 11px;
              background-size: 20px 20px;
              padding-left: 35px; background-color:#fff;
            "
            type="email"
            name="email"
            placeholder="Email"
            autocomplete="email"
            bind:value={email}
          />
          </li>
        <li>
          <button type="button" class="free-quote-button" on:click={addRes}>
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

<style>
  .hero-contact-form {
    text-align: -webkit-center;
  }
  .contact-form {
    height: 350px;
    padding: 20px 30px 30px 30px;
    border-radius: 15px;
    background: #fff;
    box-shadow: 0 16px 37px -22px rgba(2, 2, 2, 0.32);
    box-shadow: 0 3px 14px -1px rgba(0, 0, 0, 0.2);
    width: 300px;
  }

  .contact-form h2 {
    line-height: 1.5;
    font-size: 18px;
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
    color: #1a2a38 !important;
    border: 1px solid #e4e4e4;
    background: #f5f5f5;
    box-shadow: 2px 2px 3px #bfbfbf4d;
  }
  .free-quote-button {
    background: #ffe91e;
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
