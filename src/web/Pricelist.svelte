<script>
  import LP_JSON from "../assets/lp.json";
  import { perma } from "../services/store";
</script>

<section id="pricelist" class="mt-5 price-bg">
  <div class="container">
    <table>
      <tr>
        <td colspan="3">
          <h2 class="title mb-0">DENTAL IMPLANT PRICE LIST</h2>
        </td></tr
      >
      <tr>
        <td class="logo-td">
          <img
            class="price-logo"
            src="/assets/images/price-list2/osstem.png"
            alt=""
          />
        </td>
        <td> OSSTEM® Dental Implant + Abutment </td>
        <td class="price"> {LP_JSON[$perma]["osstem-price"]} </td>
      </tr>
      <tr>
        <td class="logo-td">
          <img
            class="price-logo"
            src="/assets/images/price-list2/straumann.png"
            alt=""
          />
        </td>
        <td> Straumann® Dental Implant + Abutment </td>
        <td class="price"> {LP_JSON[$perma]["straumann-price"]}</td>
      </tr>
      <tr>
        <td class="logo-td">
          <img
            class="price-logo"
            src="/assets/images/price-list2/megagen.png"
            alt=""
          />
        </td>
        <td> Megagen® Dental Implant + Abutment </td>
        <td class="price">
          <span class="old-price"
            >{LP_JSON[$perma]["megagen-price-old"]}
          </span>{LP_JSON[$perma]["megagen-price"]}
        </td>
      </tr>
      <tr>
        <td class="logo-td">
          <img
            class="price-logo"
            src="/assets/images/price-list2/nucleoss.png"
            alt=""
          />
        </td>
        <td> NucleOss® Dental Implant + Abutment </td>
        <td class="price"> {LP_JSON[$perma]["nucleoss-price"]}</td>
      </tr>
    </table>
  </div>
</section>

<style>
  .price-bg {
    background-color: #fff;
    box-shadow: 0px 0px 14px 0 rgb(97 97 97 / 26%);
  }
  table {
    border-collapse: collapse;
  }

  tr {
    border-bottom: 1px solid #cfcfcf;
    height: 120px;
  }
  td {
    font-size: 18px;
  }
  td img {
    width: fit-content;
    max-height: 70px;
    vertical-align: middle;
  }
  .logo-td {
    width: 250px;
    text-align: center;
  }
  .old-price {
    text-decoration-line: line-through;
    padding-right: 10px;
    color: #ffe91e;
  }
  .price {
    padding-right: 2rem;
    text-align: right;
    font-weight: 500;
    font-size: 22px;
  }
</style>
