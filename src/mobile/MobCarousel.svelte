<script>
  import Carousel from "svelte-carousel";
</script>

<div class="container img-header">
  <div class="rows   ">
    <div class=" img-text ">
      <div class="">
        <h2 class="image-header title text-center">
          Armada Smile Dental <br /> Antalya / Turkey
        </h2>
      </div>
    </div>
  </div>
</div>
<div class="box-container">
  <div class="box">
    <div class="container">
      <div class="outerb">
        <div class="rows">
          <Carousel particlesToShow={1} particlesToScroll={1} dots={false}>
            <div>
              <div class="review-container">
                <div class="small-image">
                  <img
                    class="small-image"
                    src="/assets/images/clinic/1.webp"
                    alt=""
                  />
                </div>
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/2.webp"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/3.webp"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/4.webp"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/5.webp"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/6.webp"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/7.webp"
                  alt=""
                />
              </div>
            </div>
            <div class="review-container">
              <div class="small-image">
                <img
                  class="small-image"
                  src="/assets/images/clinic/8.webp"
                  alt=""
                />
              </div>
            </div>
          </Carousel>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .img-header {
    margin-top: 120px;
  }
  .box-container {
    text-align: -webkit-center;
  }
  .box .outerb {
    margin-left: 5px;
    margin-right: 5px;
    background: #ffffff;
    border-radius: 10px;
    box-shadow: 0 3px 14px -1px rgba(0, 0, 0, 0.2);
  }
  .img-header {
    margin-top: 220px;
  }
  .review-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;

    padding-top: 30px;
    padding-bottom: 30px;
  }
  .small-image {
    width: 100%;
  }
  h2 {
    font-size: 21px;
    line-height: 1.4;
    color:#273c56 !important
  }
</style>
