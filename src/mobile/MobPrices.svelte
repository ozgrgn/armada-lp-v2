<script>
    import AniButton from "../components/AniButton.svelte";

</script>
<section id="pricelist" class="mt-4 price-bg">
  <div class="container">
    <table>
      <tr>
        <td colspan="3">
          <h2 class="title mb-0">IMPLANT TREATMENTS PRICES</h2>
        </td></tr
      >
      <tr>
        <td class="logo-td">
          <img
            class="price-logo"
            src="/assets/images/price-list2/osstem.png"
            alt=""
            loading="lazy"
          />
        </td>
        <td> OSSTEM® Dental <br /> Implant + Abutment </td>
        <td class="price">
         <span>£ 350 </span>
        </td>
      </tr>
      <tr>
        <td class="logo-td">
          <img
            class="price-logo"
            src="/assets/images/price-list2/straumann.png"
            alt=""
            loading="lazy"
          />
        </td>
        <td> Straumann® Dental <br /> Implant + Abutment </td>
        <td class="price"> £ 690</td>
      </tr>
      <tr>
        <td class="logo-td">
          <img
            class="price-logo"
            src="/assets/images/price-list2/megagen.png"
            alt=""
            loading="lazy"
          />
        </td>
        <td> Megagen® Dental <br /> Implant + Abutment </td>
        <td class="price"> <span class="old-price">£ 540 <br /> </span>  £ 450 </td>
      </tr>
      <tr>
        <td class="logo-td">
          <img
            class="price-logo"
            src="/assets/images/price-list2/nucleoss.png "
            alt=""
            loading="lazy"
          />
        </td>
        <td> NucleOss® Dental <br /> Implant + Abutment </td>
        <td class="price"> £ 300</td>
      </tr>
   <tr>    <div class="tab-button pt-4 ">
    <AniButton/>
   </div></tr>
    </table>

  </div>
</section>

<style>
      .tab-button {
    display: flex;
    flex-direction: column;
    z-index: 999999999;
  }
  h2 {
    line-height: 1.3;
  }
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
    font-size: 17px;
  }
  td img {
  
    max-height: 35px;
    vertical-align: middle;
  }
  .logo-td {
    text-align: center;
  }
  .old-price {
    text-decoration-line: line-through;
    color: #ba4e5b;
  }
  .price {
    width: 50px;
    text-align: right;
    font-weight: 500;
    font-size: 16px;
  }
</style>
