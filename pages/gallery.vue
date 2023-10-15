<template>
  <div class="mx-auto bg-info" style="width: 700px;">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
    >
      <!-- Text slides with image -->
      <div v-for="(image, index) in images" :key="`image-${index}`">
        <b-carousel-slide
          :text="image.title"
          :img-src="image.url"
        />
      </div>
    </b-carousel>
  </div>
</template>

<script>
export default {
  name: 'GalleryComponent',

  async asyncData ({ $http }) {
    const res = await $http.$get('https://jsonplaceholder.typicode.com/albums/1/photos')
    // eslint-disable-next-line no-console
    return {
      images: res
    }
  }
}
</script>
