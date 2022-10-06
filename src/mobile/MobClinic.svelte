<script>
    let showModal = false;
  
    function toggleModal() {
      showModal = !showModal;
    }
    function closeModal() {}
  </script>
  
  <section id="clinic">
    <div on:click={closeModal}>
      <div class="relative  pt-4 pb-3 overflow-hidden">
        <div class="relative">
          <div
            class="lg:mx-auto lg:max-w-7xl lg:px-8 lg:grid lg:grid-cols-2 lg:grid-flow-col-dense lg:gap-24 md:h-80 lg:h-80	"
          >
            <div
              class="px-4 max-w-xl mx-auto sm:px-6 lg:max-w-none lg:mx-0 lg:px-0 flex flex-col self-center			"
            >
              <!-- <div>
                <div class="">
                  <h2
                    class="text-3xl font-extrabold tracking-tight text-gray-700"
                  >
                    ARMADA SMILE CLINIC
                  </h2>
            
                </div>
              </div> -->
            </div>
            <div
              class="mt-12 lg:mt-0 mt-16 flex justify-center flex-col self-center "
            >
              <div class="" on:click={toggleModal}>
                <img
                  class="w-100 h-auto"
                  style="left:0; border-radius:0.75rem; box-shadow: 3px 3px 8px 0 rgba(97, 97, 97, 0.5);"
                  src="/assets/images/armada-smile.webp"
                  alt="Armada Smile 3D"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
  
      {#if showModal}
        <div class="modal" style="">
          <div class="modal-content">
            <!--content-->
            <div class="modal-header">
              <!--header-->
              <div class="modal-title">
                <h3>ARMADA SMILE CLINIC</h3>
                <button class="modal-close-button" on:click={toggleModal}>
                  <span class="modal-close"> × </span>
                </button>
              </div>
              <!--body-->
              <div class="iframe-box ">
                <iframe
                id="ds"
                  title="armada-smile"
                  style="width:90vw  ;height:90vh;mx-5"
                  src="https://my.matterport.com/show/?m=xbZRPcPkpvr&play=1"
                  frameborder="0"
                  allowfullscreen={false}
                  allow="xr-spatial-tracking"   />
              </div>
            </div>
            <!--footer-->
          </div>
        </div>
  
        <div class="overlay opacity-25 fixed inset-0 z-40 bg-black"/>
      {/if}
    </div>
  </section>
  
  <style>
    
    .overlay {
      opacity: 0.25;
      background-color: black;
      z-index: 1900;
      top: 0px;
      right: 0px;
      bottom: 0px;
      left: 0px;
      position: fixed;
    }
  
    .modal {
      overflow-x: hidden;
      overflow-y: auto;
      justify-content: center;
      align-items: center;
      display: flex;
      z-index: 2000;
      top: 0px;
      right: 0px;
      bottom: 0px;
      left: 0px;
      position: fixed;
    }
    .modal-content {
      margin-top: 1.5rem;
      margin-bottom: 1.5rem;
      margin-left: auto;
      margin-right: auto;
      position: relative;
    }
    .modal-header {
      width: 100%;
      flex-direction: column;
      border-width: 0px;
      outline-offset: 2px;
      outline-offset: 2px;
      background-color: white;
      flex-direction: column;
      display: flex;
      position: relative;
    }
  
    .modal-title {
      padding: 1rem;
      border-color: rgb(226 232 240);
      border-style: solid;
      border-width: 0px;
      border-bottom-width: 1px;
      border-top-left-radius: 0.25rem;
      border-top-right-radius: 0.25rem;
      justify-content: space-between;
      align-items: flex-start;
      display: flex;
    }
    h3 {
      font-weight: 600;
      font-size: 1.25rem;
      list-style: 1.75rem;
      margin: 0;
    }
    .modal-close-button {
      color: rgb(55 65 81);
      line-height: 0.75rem;
      font-size: 1.5rem;
      background-color: transparent;
      border: none;
      font-weight: 600;
      cursor: pointer;
      padding: 0.25rem;
    }
    .modal-close {
      width: 1.5rem;
      height: 1.5rem;
      display: block;
      background-color: transparent;
      line-height: 1.5rem;
      font-size: 1.5rem;
    }
  </style>
  