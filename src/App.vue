<template>
    <h1>Ciao Mondo</h1>
    <img class="immagine" v-for="(immagine, index) in immagini" :src="getImageUrl(immagine)" :key="`immagine-${index}`" />

</template>


<script>
  export default {
    data() {
      return {
        immagini: [
          'immagine.jpg',
          'immagine_2.jpg'
        ]
      }
    },
    methods: {
      getImageUrl(name) {
        return new URL(`./assets/${name}`, import.meta.url).href;
      }
    }
  }
</script>


<style lang="scss">
  @use './styles/general.scss' as *;

  //se mi riferisco ad una immagine qua, ad esempio per una background-image, devo riferirmi alla path relativa


</style>