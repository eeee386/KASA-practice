<template>
  <div class="card-wrapper" v-bind:class="card.classes && card.classes.cardWrapper">
    <img v-if="card.img" class="card-image" :src=card.img.src :alt=card.img.alt :title=card.img.title>
    <div v-if="card.thumbnail || card.title || card.subTitle" class="card-title-part">
      <img v-if="card.thumbnail" class="card-thumbnail" :src=card.thumbnail.src :alt=card.thumbnail.alt :title=card.thumbnail.title>
      <div v-if="card.title || card.subTitle" class="card-title-subtitle">
        <h3 v-if="card.title" class="card-title">{{ card.title }}</h3>
        <h4 v-if="card.subTitle" class="card-subtitle">{{ card.subTitle }}</h4>
      </div>
    </div>
    <div class="card-content" v-html="card.content"/>
    <div v-if="card.footer" class="card-footer" v-html="card.footer"/>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    card: {
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
      },
      classes: {
        cardWrapper:  String,

      }
    }
  }
}
</script>

<style scoped>
.card-wrapper {
  width: 327px;
  display: flex;
  flex-direction: column;
  border: 1px solid rgba(45, 45, 45, 0.2);
  border-radius: 4px;
}

.card-image {
  object-fit: cover;
}

.card-content {
  overflow: hidden;
  margin: 24px;
  height: 140px;
}

.card-footer {
  height: 68px;
  display: flex;
  align-items: center;
  border-top: 1px solid rgba(45, 45, 45, 0.2);
}

.card-title-part {
  margin-top: 24px;
  margin-left: 24px;
  display: flex;
}

.card-thumbnail {
  border-radius: 50%;
}

.card-title-subtitle{
  display:flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 24px;
}

.card-title {
  font-family: Lora,serif;
  font-style: normal;
  font-weight: bold;
  font-size: 20px;
  line-height: 28px;
  color: #2D2D2D;
  margin: 0;
}

.card-subtitle {
  margin: 0;
  font-family: Roboto,serif;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  color: #6E6E6E;
}
</style>

<style>
.card-content * {
  text-overflow: ellipsis;
  height: 140px;
  margin:0;
}
.card-footer * {
  margin-left: 24px;
}
</style>