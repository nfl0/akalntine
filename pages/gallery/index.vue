<template>
  <div class="container">
    <!-- {{ gallery }} -->
    <h1 class="heading">
      Gallery
    </h1>
    <section v-for="ga in gallery.slice().reverse()" :key="ga.title" class="allth">
      <h4 class="title">
        {{ ga.title }}
      </h4>
      <div class="allimg row">
        <div v-for="im in ga.images" :key="im" class="col s12 m4 l4 img-wrapper">
          <img :src="im" class="img" loading="lazy">
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  fetch ({ store }) {
    // const psts = []
    return axios.get('https://raw.githubusercontent.com/nfl0/webdata/master/gallery.json')
      .then(async ({ data }) => {
        /* eslint-disable no-console */
        // console.log(data.gallery)
        await store.commit('Gallery', data.gallery)
      })
      .then(() => {
      })
  },
  computed: {
    gallery () {
      return this.$store.state.gallery
    }
  },
  head () {
    return {
      title: 'Galerie - Association Akal Ntine Dartanout',
      meta: [
        { hid: 'description', name: 'description', content: 'Galerie photos des événements et activités de l Association Akal Ntine Dartanout' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  .heading{
    margin: 16px;
    font-size: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    font-family: sans-serif;
    font-size: 32px;
    font: Bolder 40px/43px Source Sans Pro;
  }
  .allth{
    color: black;
    width: auto;

    .title{
      font-size: 28px;
      color: rgb(53, 52, 52);
      display: inline-block;
      padding-bottom: 12px;
      font-weight: bold;
      margin-left: 16px;
      border-bottom: solid 4px $primary-color;
    }
    .img-wrapper {
      padding: 10px;

      .img{
        height: 200px;
        display: inline-block;
        width: 100%;
        object-fit: cover;
        /*box-shadow: 5px 5px 5px rgba(0, 0, 255, 0.5);*/
        border-radius: 5px;
        transition: box-shadow 0.25s ease-in-out;
        box-sizing: border-box;
        box-shadow: 0 0 10px rgba(100, 100, 100, 0.5);
        cursor: pointer;

        &:hover {
          box-shadow: 0 0 2px rgba(100, 100, 100, 0.5);
        }
      }
      @media screen and (min-width: 600px) {
        .img {height: 200px;}
      }
    }
  }
}
</style>
