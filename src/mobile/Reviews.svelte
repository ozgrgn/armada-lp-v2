<script>
  import Carousel from "svelte-carousel";

  export let filteredReviews;
  filteredReviews = [
    {
      _id: "6311c4e2e93fc0079c0c21ec",
      reviewLang: "en",
      reviewSort: 1,
      reviewName: "Jackson Szymanowski",
      reviewDate: "22.08.2022",
      reviewPlatform: "TrustPilot",
      reviewText:
        "I want to say how if you have had a fear of the dentist 🦷 then your fear will be taken away with Armada they are professional and have your 100%care in there power from the start of you getting on your plane to the hotel ,and all your fantastic communication skills by the lovely 🌹 gorgeous Gamze and Ozzie they are amazing at keeping you updated with every step of the journey to having that final result of pearly perfect teeth can't thank you all enough and for the record it's so true what Gamze and Ozzie say you really don't feel a thing thank you all once again wish I'd of come to you months and months ago 🙏❤️🦷",
      reviewLink: "https://www.trustpilot.com/users/630382a74e17bf0013d4e3f7",
      created_at: "2022-09-02T08:54:58.917Z",
      updated_at: "2022-09-02T08:54:58.917Z",
      __v: 0,
    },
    {
      _id: "63111e21e5a2ce978e25146a",
      reviewLang: "en",
      reviewSort: 10,
      reviewName: "Isabelle Williams",
      reviewDate: "29.08.2022",
      reviewPlatform: "Google",
      reviewText:
        "When i contacted Armada Smile they got back to me instantly provided me with every information that i needed and made feel very comfortable which was the most important thing to me. Its a decision that i wish i have made years ago. I am so happy to meet a lovely team of people and thank you for making me feel like i was at home.",
      created_at: "2022-09-01T21:03:29.664Z",
      updated_at: "2022-09-02T08:44:18.192Z",
      __v: 0,
      reviewLink: "https://g.co/kgs/FJStkH",
      reviewStars: "disabled",
      reviewAvatar: "1ceuBcG_vf.png",
    },
    {
      _id: "63111db4e5a2ce978e251466",
      reviewLang: "en",
      reviewSort: 9,
      reviewName: "James Marshall",
      reviewDate: "25.08.2022",
      reviewPlatform: "Google",
      reviewText:
        "I can say i have had the most luxurious experience ever. I was never confident enough to smile and wouldn’t socialise becuase i was always embarassed. I would like to say thank you alot to Armada Smile team very professional. The finished smile i wanted was way better than what i wanted, beyond my expectations. Highly recommend to anyone that is looking for that new pearly smile!",
      created_at: "2022-09-01T21:01:40.599Z",
      updated_at: "2022-09-02T08:45:04.878Z",
      __v: 0,
      reviewLink: "https://g.co/kgs/pT6ZKw",
      reviewStars: "disabled",
      reviewAvatar: "Tawquoz3rl.png",
    },
    {
      _id: "63111d5ce5a2ce978e251452",
      reviewLang: "en",
      reviewSort: 8,
      reviewName: "Sam Hearn",
      reviewDate: "01.08.2022",
      reviewPlatform: "Google",
      reviewText:
        "For over 10 years i have battled so much with myself, could not smile, was always covering my mouth. Now on my way back to 🇮🇪 and can’t stop smiling. In tears of happiness, recommend this place to anyone! Thank you so much Armada Smile.",
      created_at: "2022-09-01T21:00:12.397Z",
      updated_at: "2022-09-02T08:47:20.739Z",
      __v: 0,
      reviewLink: "https://g.co/kgs/71iQ7X",
      reviewStars: "disabled",
      reviewAvatar: "iFWeip71s4.png",
    },
    {
      _id: "63111cf6e5a2ce978e251446",
      reviewLang: "en",
      reviewSort: 7,
      reviewName: "Tiana Bate",
      reviewPlatform: "Google",
      reviewText:
        "Can i firstly say how amazing these people are with everything they have done for me. I have been researching to have dental Implants and i must say i am delighted to be treated at Armada Smile. This clinic is the most genuine clinic i have come across after all my researches. Wouldnt even think twice, very very professional and the quality they provide is 10/10.",
      created_at: "2022-09-01T20:58:30.170Z",
      updated_at: "2022-09-02T08:48:31.199Z",
      __v: 0,
      reviewDate: "11.08.2022",
      reviewStars: "disabled",
      reviewLink: "https://g.co/kgs/mEzsTQ",
      reviewAvatar: "roE1Ci2yLM.png",
    },
    {
      _id: "63111bbee5a2ce978e251427",
      reviewLang: "en",
      reviewSort: 5,
      reviewName: "Carl Birkenshaw",
      reviewDate: "25.03.2022",
      reviewPlatform: "Google",
      reviewText:
        "So happy with result all done in 5 days after 20 years I have my smile back thank you for all you help and what you have done 9 implants and 24 crowns amazing now pain at all",
      created_at: "2022-09-01T20:53:18.892Z",
      updated_at: "2022-09-02T08:51:16.280Z",
      __v: 0,
      reviewStars: "disabled",
      reviewLink:
        "https://www.google.com/maps/reviews/data=!4m8!14m7!1m6!2m5!1sChdDSUhNMG9nS0VJQ0FnSUNXa3RLZzVBRRAB!2m1!1s0x0:0x336ea104e4a18dbd!3m1!1s2@1:CIHM0ogKEICAgICWktKg5AE%7CCgwI--_SkAYQwNH4vwI%7C?hl=en-US",
      reviewAvatar: "_xoKnTlu0y.png",
    },
    {
      _id: "62d484bb8857101ea79d5ae1",
      reviewLang: "en",
      reviewSort: 2,
      reviewName: "KyeSho",
      reviewDate: "11.08.2022",
      reviewPlatform: "TrustPilot",
      reviewText:
        "OH MY GOD! Back in the UK after my treatment and amazing 7 days that i have spent in Antalya. I have people complimenting my new bright teeth already since i landed. I could never express enough appreciation to this clinic and its team! I had full mouth Implants and 24 Zirconium crowns, I have not felt any pain during my surgery AT ALL! The care ive been given has been first class. Such a respectful team with big smiles on their face every time i stepped into this clinic. They listen to you and take into account everything that is important to you. I have picked this clinic out of all the other options out there because Armada Smile is after quality and not quantity. As someone concerned about traveling abroad for dental treatment.I would not hesitate to recommend them to anyone.I wish them the best of luck and success.",
      reviewLink: "https://www.trustpilot.com/users/62f4d139a86c6400125f0c35",
      created_at: "2022-07-17T21:52:59.502Z",
      updated_at: "2022-09-01T20:44:34.952Z",
      __v: 0,
      reviewStars: "5",
    },
    {
      _id: "62d47cba8857101ea79d5a78",
      reviewLang: "en",
      reviewSort: 3,
      reviewName: "Callum H",
      reviewDate: "26.07.2022",
      reviewPlatform: "TrustPilot",
      reviewText:
        "The clinic is very professional and I didn’t actually expect to get my full mouth implants done in turkey but the price was reasonable and it was all worth the experience. The doctor did my job very carefully and did what I liked for me with patience. During the treatment it was a hassle free experience the team managed everything regarding the hotel and transfer very well. The environment was friendly and the clinic was in a really nice spot. For me it was a beautiful experience I thank so much for Dr. Sayaf and his team I am completely satisfied with my teeth and I’m pleased to get my smile back. The doctor knows his job well.",
      reviewLink: "https://www.trustpilot.com/users/62dfb036327477001438149f",
      created_at: "2022-07-17T21:18:50.915Z",
      updated_at: "2022-09-01T20:45:51.691Z",
      __v: 0,
      reviewStars: "5",
    },
    {
      _id: "62d1dfa9a741faa82c4db36e",
      reviewName: "Joe M",
      reviewDate: "14.07.2022",
      reviewPlatform: "TrustPilot",
      reviewText:
        "Wow! Been in contact with Armada Smile for around 3 months. I wasent really sure on booking at first but I shouldn't have been. Im glad I got my smile back after a really long time in the UK. I wasn’t expecting how little pain there was after the injections of the course. I haven’t always been that confident with myself and have avoided going to the dentists for years. So glad after having missing teeth and broken teeth my new smile is so good and I feel so confident. The service was also Immaculate I thank the whole Armada Smile Studio Team.",
      reviewLink: "https://www.trustpilot.com/users/62cffa2dbb44fa001349b62b",
      created_at: "2022-07-15T21:44:09.705Z",
      updated_at: "2022-09-01T20:47:20.222Z",
      __v: 0,
      reviewStars: "5",
      reviewLang: "en",
      reviewSort: 4,
    },
    {
      _id: "62ceac75355bffb007fb3dec",
      reviewName: "Hannah Taylor",
      reviewDate: "24.08.2022",
      reviewPlatform: "Google",
      reviewText:
        "I cant praise this clinic enough. I have been scared of the dentist all my life, after making the decision to finally wanting to smile, i came to Turkey from the Uk. The end result was amazing. The level of professionalism, the service was amazing. Having a staff of native English speakers is a great benefit also. My dental treatment and time in Antalya was a dream,including the hotel and transfer services. These guys are brilliant.",
      reviewLink: "https://g.co/kgs/YMf6Ry",
      created_at: "2022-07-13T11:28:53.593Z",
      updated_at: "2022-09-01T21:38:34.722Z",
      __v: 0,
      reviewStars: "5",
      reviewLang: "en",
      reviewSort: 6,
      reviewAvatar: "6i5IvJJpjP.png",
    },
  ];

  let toShow;
  let toScroll;
  let dots;
  if (window.innerWidth <= 640) {
    toShow = 1;
    toScroll = 1;
  } else {
    toShow = 4;
    toScroll = 3;
  }
</script>

<!-- REVIEWS -->
<div class="box  md:mx-0 hidden-xs pt-4 pb-5">
  <div class="container ">
    <div class="outerb">
      <div class="rows">
        <Carousel
          particlesToShow={toShow}
          particlesToScroll={toScroll}
          dots={true}
          autoplay
          autoplayDuration={5000}
          pauseOnFocus
        >
          {#each filteredReviews as review}
            <div class="review-container">
              <a
                class="review-header "
                rel="external"
                href={review.reviewLink}
                target="_blank"
              >
                <div class="review-avatar">
                  <div
                    class="review-avatar-bg  text-center "
                  >
                    {#if review.reviewAvatar}
                      <img
                        src={`https://super--bucket.s3.eu-west-3.amazonaws.com/${review.reviewAvatar}`}
                        alt=""
                        width="44"
                        height="44"
                        class="ReviewAvatar__Avatar-sc-1lraoly-2 TOyBs"
                      />
                    {:else}
                      {review.reviewName.charAt(0)}
                    {/if}
                  </div>
                </div>
                <div class="review-info">
                  <span class="review-author">{review.reviewName}</span>
                  <div class="review-info2">
                    <div class="ratings">
                      <div class="empty-stars" />
                      <div
                        class="full-stars-tp {review.reviewPlatform == 'Google'
                          ? 'g-color'
                          : review.reviewPlatform == 'TrustPilot'
                          ? 't-color'
                          : review.reviewPlatform == 'Facebook'
                          ? 'f-color'
                          : ''} {review.reviewStars == 1
                          ? 'w-1/5'
                          : review.reviewStars == 2
                          ? 'w-2/5'
                          : review.reviewStars == 3
                          ? 'w-3/5'
                          : review.reviewStars == 4
                          ? 'w-4/5'
                          : 'w-full'}"
                      />
                      <img
                        style="width:85px"
                        src="assets/images/reviews/stars.svg"
                        alt=""
                      />
                    </div>
                    <div class="review-date hidden xl:block">
                      {review.reviewDate}
                    </div>
                  </div>
                </div></a
              >
              <div class="review-text">
                <div class="review-text-outer">
                  <div class="review-text-inner">
                    <div>
                      {review.reviewText}
                    </div>
                  </div>
                </div>
              </div>
              <a href={review.reviewLink} target="_blank">
                <div class="review-readmore">read more</div></a
              >
              <a
                class="review-link"
                href={review.reviewLink}
                target="_blank"
                rel="noopener noreferrer nofollow"
                ><div class="review-logo-container">
                  <div class="review-postedon">Posted On</div>
                  <div title="Google" class="review-icon ">
                    <div>
                      {#if review.reviewPlatform == "Google"}
                        <svg
                          class="pt-1"
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 270 90"
                          ><path
                            fill="#EA4335"
                            d="M115.75 47.18c0 12.77-9.99 22.18-22.25 22.18s-22.25-9.41-22.25-22.18C71.25 34.32 81.24 25 93.5 25s22.25 9.32 22.25 22.18zm-9.74 0c0-7.98-5.79-13.44-12.51-13.44S80.99 39.2 80.99 47.18c0 7.9 5.79 13.44 12.51 13.44s12.51-5.55 12.51-13.44z"
                          /><path
                            fill="#FBBC05"
                            d="M163.75 47.18c0 12.77-9.99 22.18-22.25 22.18s-22.25-9.41-22.25-22.18c0-12.85 9.99-22.18 22.25-22.18s22.25 9.32 22.25 22.18zm-9.74 0c0-7.98-5.79-13.44-12.51-13.44s-12.51 5.46-12.51 13.44c0 7.9 5.79 13.44 12.51 13.44s12.51-5.55 12.51-13.44z"
                          /><path
                            fill="#4285F4"
                            d="M209.75 26.34v39.82c0 16.38-9.66 23.07-21.08 23.07-10.75 0-17.22-7.19-19.66-13.07l8.48-3.53c1.51 3.61 5.21 7.87 11.17 7.87 7.31 0 11.84-4.51 11.84-13v-3.19h-.34c-2.18 2.69-6.38 5.04-11.68 5.04-11.09 0-21.25-9.66-21.25-22.09 0-12.52 10.16-22.26 21.25-22.26 5.29 0 9.49 2.35 11.68 4.96h.34v-3.61h9.25zm-8.56 20.92c0-7.81-5.21-13.52-11.84-13.52-6.72 0-12.35 5.71-12.35 13.52 0 7.73 5.63 13.36 12.35 13.36 6.63 0 11.84-5.63 11.84-13.36z"
                          /><path
                            fill="#34A853"
                            d="M225 3v65h-9.5V3h9.5z"
                          /><path
                            fill="#EA4335"
                            d="M262.02 54.48l7.56 5.04c-2.44 3.61-8.32 9.83-18.48 9.83-12.6 0-22.01-9.74-22.01-22.18 0-13.19 9.49-22.18 20.92-22.18 11.51 0 17.14 9.16 18.98 14.11l1.01 2.52-29.65 12.28c2.27 4.45 5.8 6.72 10.75 6.72 4.96 0 8.4-2.44 10.92-6.14zm-23.27-7.98l19.82-8.23c-1.09-2.77-4.37-4.7-8.23-4.7-4.95 0-11.84 4.37-11.59 12.93z"
                          /><path
                            fill="#4285F4"
                            d="M35.29 41.41V32H67c.31 1.64.47 3.58.47 5.68 0 7.06-1.93 15.79-8.15 22.01-6.05 6.3-13.78 9.66-24.02 9.66C16.32 69.35.36 53.89.36 34.91.36 15.93 16.32.47 35.3.47c10.5 0 17.98 4.12 23.6 9.49l-6.64 6.64c-4.03-3.78-9.49-6.72-16.97-6.72-13.86 0-24.7 11.17-24.7 25.03 0 13.86 10.84 25.03 24.7 25.03 8.99 0 14.11-3.61 17.39-6.89 2.66-2.66 4.41-6.46 5.1-11.65l-22.49.01z"
                          /></svg
                        >
                      {:else}
                        <svg
                          class="w-12"
                          height="-437"
                          viewBox="20.5 248.5 600 147.3"
                          width="100"
                          xmlns="http://www.w3.org/2000/svg"
                          ><path
                            d="m178.2 300.7h60.7v11.3h-23.9v63.7h-13.1v-63.7h-23.8zm58.1 20.7h11.2v10.5h.2c.4-1.5 1.1-2.9 2.1-4.3s2.2-2.7 3.7-3.8c1.4-1.2 3-2.1 4.8-2.8 1.7-.7 3.5-1.1 5.3-1.1 1.4 0 2.4.1 2.9.1.5.1 1.1.2 1.6.2v11.5c-.8-.2-1.7-.3-2.6-.4s-1.7-.2-2.6-.2c-2 0-3.9.4-5.7 1.2s-3.3 2-4.7 3.5c-1.3 1.6-2.4 3.5-3.2 5.8s-1.2 5-1.2 8v25.8h-12zm86.8 54.3h-11.8v-7.6h-.2c-1.5 2.8-3.7 4.9-6.6 6.6s-5.9 2.5-8.9 2.5c-7.1 0-12.3-1.7-15.5-5.3-3.2-3.5-4.8-8.9-4.8-16v-34.5h12v33.3c0 4.8.9 8.2 2.8 10.1 1.8 2 4.4 3 7.7 3 2.5 0 4.6-.4 6.3-1.2s3.1-1.8 4.1-3.1c1.1-1.3 1.8-2.9 2.3-4.7s.7-3.8.7-5.9v-31.5h12v54.3zm20.4-17.4c.4 3.5 1.7 5.9 4 7.4 2.3 1.4 5.1 2.1 8.3 2.1 1.1 0 2.4-.1 3.8-.3s2.8-.5 4-1c1.3-.5 2.3-1.2 3.1-2.2s1.2-2.2 1.1-3.7-.6-2.8-1.7-3.8-2.4-1.7-4-2.4c-1.6-.6-3.5-1.1-5.6-1.5s-4.2-.9-6.4-1.4-4.4-1.1-6.5-1.8-3.9-1.6-5.6-2.9c-1.6-1.2-3-2.7-3.9-4.6-1-1.9-1.5-4.1-1.5-6.9 0-3 .7-5.4 2.2-7.4 1.4-2 3.3-3.6 5.5-4.8s4.7-2.1 7.4-2.6 5.3-.7 7.7-.7c2.8 0 5.5.3 8 .9s4.9 1.5 6.9 2.9c2.1 1.3 3.8 3.1 5.1 5.2 1.4 2.1 2.2 4.7 2.6 7.7h-12.5c-.6-2.9-1.9-4.8-3.9-5.8-2.1-1-4.4-1.5-7.1-1.5-.8 0-1.9.1-3 .2-1.2.2-2.2.4-3.3.8-1 .4-1.9 1-2.6 1.7s-1.1 1.7-1.1 2.9c0 1.5.5 2.6 1.5 3.5s2.3 1.6 4 2.3c1.6.6 3.5 1.1 5.6 1.5s4.3.9 6.5 1.4 4.3 1.1 6.4 1.8 4 1.6 5.6 2.9c1.6 1.2 3 2.7 4 4.5s1.5 4.1 1.5 6.7c0 3.2-.7 5.9-2.2 8.2-1.5 2.2-3.4 4.1-5.7 5.5s-5 2.4-7.8 3.1c-2.9.6-5.7 1-8.5 1-3.4 0-6.6-.4-9.5-1.2s-5.5-2-7.6-3.5c-2.1-1.6-3.8-3.5-5-5.9-1.2-2.3-1.9-5.1-2-8.4h12.1v.1zm39.5-36.9h9.1v-16.4h12v16.3h10.8v8.9h-10.8v29c0 1.3.1 2.3.2 3.3.1.9.4 1.7.7 2.3.4.6 1 1.1 1.7 1.4.8.3 1.8.5 3.2.5.8 0 1.7 0 2.5-.1s1.7-.2 2.5-.4v9.3c-1.3.2-2.6.3-3.9.4-1.3.2-2.5.2-3.9.2-3.2 0-5.7-.3-7.6-.9s-3.4-1.5-4.5-2.6c-1.1-1.2-1.8-2.6-2.2-4.3s-.6-3.8-.7-6v-32h-9.1v-9.1zm40.3 0h11.3v7.4h.2c1.7-3.2 4-5.4 7-6.8s6.2-2.1 9.8-2.1c4.3 0 8 .7 11.2 2.3 3.2 1.5 5.8 3.5 7.9 6.2 2.1 2.6 3.7 5.7 4.7 9.2s1.6 7.3 1.6 11.2c0 3.7-.5 7.2-1.4 10.6-1 3.4-2.4 6.5-4.3 9.1s-4.3 4.7-7.3 6.3-6.4 2.4-10.4 2.4c-1.7 0-3.5-.2-5.2-.5s-3.4-.8-5-1.5-3.1-1.6-4.4-2.7c-1.4-1.1-2.5-2.4-3.4-3.8h-.2v27.1h-12v-74.4zm41.9 27.2c0-2.4-.3-4.8-1-7.1-.6-2.3-1.6-4.3-2.9-6.1s-2.9-3.2-4.7-4.3c-1.9-1.1-4.1-1.6-6.5-1.6-5 0-8.8 1.7-11.4 5.2-2.5 3.5-3.8 8.2-3.8 14 0 2.8.3 5.3 1 7.6s1.6 4.3 3 6c1.3 1.7 2.9 3 4.8 4s4 1.5 6.5 1.5c2.8 0 5-.6 6.9-1.7s3.4-2.6 4.7-4.3c1.2-1.8 2.1-3.8 2.6-6.1.5-2.4.8-4.7.8-7.1zm21.1-47.9h12v11.3h-12zm0 20.7h12v54.3h-12zm22.7-20.7h12v75h-12zm48.6 76.5c-4.3 0-8.2-.7-11.6-2.2s-6.2-3.4-8.6-5.9c-2.3-2.5-4.1-5.6-5.3-9.1s-1.9-7.4-1.9-11.5.6-7.9 1.9-11.4c1.2-3.5 3-6.5 5.3-9.1 2.3-2.5 5.2-4.5 8.6-5.9s7.3-2.2 11.6-2.2 8.2.7 11.6 2.2c3.4 1.4 6.2 3.4 8.6 5.9 2.3 2.5 4.1 5.6 5.3 9.1s1.9 7.3 1.9 11.4c0 4.2-.6 8-1.9 11.5s-3 6.5-5.3 9.1c-2.3 2.5-5.2 4.5-8.6 5.9s-7.2 2.2-11.6 2.2zm0-9.5c2.6 0 5-.6 6.9-1.7 2-1.1 3.5-2.6 4.8-4.4s2.2-3.9 2.8-6.1c.6-2.3.9-4.6.9-7 0-2.3-.3-4.6-.9-6.9s-1.5-4.3-2.8-6.1-2.9-3.2-4.8-4.3c-2-1.1-4.3-1.7-6.9-1.7s-5 .6-6.9 1.7c-2 1.1-3.5 2.6-4.8 4.3-1.3 1.8-2.2 3.8-2.8 6.1s-.9 4.6-.9 6.9c0 2.4.3 4.7.9 7s1.5 4.3 2.8 6.1 2.9 3.3 4.8 4.4c2 1.2 4.3 1.7 6.9 1.7zm31-46.3h9.1v-16.4h12v16.3h10.8v8.9h-10.8v29c0 1.3.1 2.3.2 3.3.1.9.4 1.7.7 2.3.4.6 1 1.1 1.7 1.4.8.3 1.8.5 3.2.5.8 0 1.7 0 2.5-.1s1.7-.2 2.5-.4v9.3c-1.3.2-2.6.3-3.9.4-1.3.2-2.5.2-3.9.2-3.2 0-5.7-.3-7.6-.9s-3.4-1.5-4.5-2.6c-1.1-1.2-1.8-2.6-2.2-4.3s-.6-3.8-.7-6v-32h-9.1v-9.1z"
                          /><path
                            d="m164.2 300.7h-54.9l-16.9-52.2-17 52.2-54.9-.1 44.4 32.3-17 52.2 44.4-32.3 44.4 32.3-16.9-52.2z"
                            fill="#00b67a"
                          /><path
                            d="m123.6 344.7-3.8-11.8-27.4 19.9z"
                            fill="#005128"
                          /></svg
                        >
                      {/if}
                    </div>
                  </div>
                </div></a
              >
            </div>
          {/each}
        </Carousel>
      </div>
    </div>
  </div>
</div>

<style>
  .container {
    z-index: 49;
  }
  /* REVIEWS */

  .box {
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
  .g-color {
    color: rgb(252, 191, 2) !important;
  }
  .t-color {
    color: #00b67b !important;
  }
  .f-color {
    color: #4267b2 !important;
  }
  .review-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 10px;
    padding-top: 20px;
  }
  .review-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 18px;
    padding-top: 40px;
  }
  .review-header {
    flex-wrap: nowrap !important;
    display: flex !important;
    position: static !important;
    color: inherit !important;
    max-width: 100% !important;
    text-decoration: none !important;
    border: none !important;
  }
  .review-avatar {
    flex: 0 0 auto;
    width: 44px;
    height: 44px;
    border-radius: 50%;
    overflow: hidden;
  }
  .review-avatar-bg {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    height: 100%;
    transition: opacity 1s ease-out 0s;
    background-color: rgb(210, 210, 210);
    border-radius: 50%;
    overflow: hidden;
    opacity: 1;
  }
  .review-info {
    margin-left: 16px;
    display: flex;
    flex-direction: column;
    min-width: 0px;
  }
  .review-author {
    font-size: 14px;
    font-weight: 500;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    text-align: left;
    color: rgb(17, 17, 17);
  }
  .review-info2 {
    display: flex;
    flex-wrap: wrap;
    -webkit-box-align: center;
    align-items: center;
  }
  .ratings {
    position: relative;
    vertical-align: top;
    display: inline-block;
    color: #b1b1b1;
    overflow: hidden;
  }

  .full-stars-tp {
    position: absolute;
    left: 0;
    top: 0;
    white-space: nowrap;
    overflow: hidden;
  }
  .empty-stars:before,
  .full-stars-tp:before {
    content: "\2605\2605\2605\2605\2605";
    font-size: 12pt;
  }
  .empty-stars:before {
    -webkit-text-stroke: 1px #b1b1b1;
  }

  /* Webkit-text-stroke is not supported on firefox or IE */

  /* Firefox */
  @-moz-document url-prefix() {
    .full-stars {
      color: rgb(252, 191, 2) !important;
    }
  }
  .review-date {
    padding-left: 10px;
    overflow: hidden;
    min-width: 0px;
    font-weight: 400;
    font-size: 12px;
    line-height: 1.17;
    white-space: nowrap;
    text-overflow: ellipsis;
    color: rgba(17, 17, 17, 0.5);
  }
  .review-text {
    font-weight: 400;
    margin-top: 8px;
    width: 100%;
    line-height: 1.3;
    color: rgb(17, 17, 17);
    font-size: 13px;
    text-align: left;
  }
  .review-text-outer {
    position: relative;
    overflow: hidden;
    height: 67px;
    width: 100%;
    line-height: 1.3;
    color: rgb(17, 17, 17);
    font-size: 13px;
    text-align: left;
  }
  .review-link {
    margin-top: 12px;
    display: block !important;
    position: static !important;
    color: inherit !important;
    max-width: 100% !important;
    text-decoration: none !important;
    border: none !important;
  }
  .review-postedon {
    color: rgba(17, 17, 17, 0.5);
    font-family: Montserrat;
    font-weight: 400;
    font-size: 13px;
  }
  .review-icon {
    font-size: 12px !important;
    flex: 0 1 0%;
  }
  .review-readmore {
    display: inline-block;
    cursor: pointer;
    font-size: 14px;
    color: rgba(17, 17, 17, 0.5);
  }
</style>
