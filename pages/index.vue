<template>
  <main>
    <h1>Hello World!</h1>
    <CardList v-bind:cards="cardData" />
  </main>
</template>

<script>
import CardList from '../components/CardList';

export default {
  components: {
    CardList
  },
  data() {
    return {
      cardData: [
        {
          img: {
            alt: "pic",
            src: "https://i.picsum.photos/id/844/300/200.jpg?hmac=nScDnrvjcq1VjYNAh6OKIR_tQdDSITIWW578WbADLgc",
            title: "pic",
          },
          title: "Lorem Ipsum",
          subTitle: "Lorem Ipsum",
          content: "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam iaculis tortor quis sem convallis pretium. Nulla finibus diam vel fringilla accumsan. Sed cursus commodo magna, a pulvinar arcu maximus ut. Maecenas feugiat ligula a metus tincidunt, ut feugiat orci blandit. Sed leo augue, semper porta convallis ac, ornare ut urna. Phasellus justo nunc, laoreet non neque ac, dapibus fermentum sapien. Sed suscipit dolor libero, sed ultricies est vulputate sed. Aenean malesuada, nisl ut laoreet lacinia, ex mi pharetra nibh, id vehicula orci velit eget ipsum. Maecenas ullamcorper odio et mattis lobortis. Cras ultrices ullamcorper diam ac lacinia. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nulla erat tortor, pellentesque ac ornare vel, volutpat non metus. Praesent dapibus imperdiet lectus non gravida.</p>",
          footer: "<button>Gomb</button>",
          thumbnail: {
            alt: "thumb",
            src: "https://i.picsum.photos/id/374/60/60.jpg?hmac=QL3erfWkjCOn1P83W6X8uwIRCAoWbQQCEIg2n272610",
            title: "thumb",
          },
        },
        {
          title: "Lorem Ipsum",
          content: "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam iaculis tortor quis sem convallis pretium. Nulla finibus diam vel fringilla accumsan. Sed cursus commodo magna, a pulvinar arcu maximus ut. Maecenas feugiat ligula a metus tincidunt, ut feugiat orci blandit. Sed leo augue, semper porta convallis ac, ornare ut urna. Phasellus justo nunc, laoreet non neque ac, dapibus fermentum sapien. Sed suscipit dolor libero, sed ultricies est vulputate sed. Aenean malesuada, nisl ut laoreet lacinia, ex mi pharetra nibh, id vehicula orci velit eget ipsum. Maecenas ullamcorper odio et mattis lobortis. Cras ultrices ullamcorper diam ac lacinia. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nulla erat tortor, pellentesque ac ornare vel, volutpat non metus. Praesent dapibus imperdiet lectus non gravida.</p>",
          thumbnail: {
            alt: "thumb",
            src: "https://i.picsum.photos/id/374/60/60.jpg?hmac=QL3erfWkjCOn1P83W6X8uwIRCAoWbQQCEIg2n272610",
            title: "thumb",
          },
          classes: {
            cardWrapper: "outerCardWrapper"
          }
        },
        {
          content: "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam iaculis tortor quis sem convallis pretium. Nulla finibus diam vel fringilla accumsan. Sed cursus commodo magna, a pulvinar arcu maximus ut. Maecenas feugiat ligula a metus tincidunt, ut feugiat orci blandit. Sed leo augue, semper porta convallis ac, ornare ut urna. Phasellus justo nunc, laoreet non neque ac, dapibus fermentum sapien. Sed suscipit dolor libero, sed ultricies est vulputate sed. Aenean malesuada, nisl ut laoreet lacinia, ex mi pharetra nibh, id vehicula orci velit eget ipsum. Maecenas ullamcorper odio et mattis lobortis. Cras ultrices ullamcorper diam ac lacinia. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nulla erat tortor, pellentesque ac ornare vel, volutpat non metus. Praesent dapibus imperdiet lectus non gravida.</p>",
          footer: "<button>Gomb</button>",
          classes: {
            cardWrapper: "outerCardWrapper"
          }
        },

      ]
    };
  }

}
</script>
<style>
.outerCardWrapper {
  margin-top: 24px;
}
</style>