<template>
  <div>
    <img :src=card.img.src :alt=card.img.alt :title=card.img.title>
    <img :src=card.thumbnail.src :alt=card.thumbnail.alt :title=card.thumbnail.title>
    <h3>{{card.title}}</h3>
    <h4>{{card.subTitle}}</h4>
    <div v-html="card.content" />
    <div v-html="card.footer" />
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {card:         {
      img: {
        alt: String,
        src: String,
        title: String,
      },
      title: String,
      subTitle: String,
      content: String,
      footer: String,
      thumbnail: {
        alt: String,
        src: String,
        title: String,
      }
    }}
}
</script>