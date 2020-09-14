<template>
  <div id="app">
    <CoolLightBox
      :items="items"
      :index="index"
      :effect="'fade'"
      @close="index = null"
    >
    </CoolLightBox>

    <div class="images-wrapper">
      <div
        v-for="(image, imageIndex) in items"
        :key="imageIndex"
        class="image"
        :style="{ backgroundImage: 'url(' + image + ')' }"
        @click="index = imageIndex"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        'https://cosmos-images2.imgix.net/file/spina/photo/20565/191010_nature.jpg?ixlib=rails-2.1.4&auto=format&ch=Width%2CDPR&fit=max&w=835',
        'https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/nature-quotes-1557340276.jpg?crop=0.666xw:1.00xh;0.168xw,0&resize=640:*',
      ],
      index: null,
    }
  },
}
</script>
