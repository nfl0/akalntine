<template>
  <section class="activities-page">
    <h1 class="page-title center-align">
      Activités
    </h1>
  <div class="container activities-wrapper">
    <div class="row">
      <div v-for="post in posts.slice().reverse()" :key="post.post_url" class="col s12 m6">
        <div class="card activity-card">
          <a :href="post.post_url" target="_blank">
            <div class="card-image">
              <progressive-img
                :src="post.image"
                placeholder="/imageplaceholder8x5.png"
                blur="30"
                delay="200"
                class="activity-image center-align"
              />
            </div>
            <div class="card-content">
              <h5 class="act-card-title">
                <b>{{ post.post_text }}</b>
              </h5>
              <h6 class="act-card-date">
                {{ post.time }}
              </h6>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
  </section>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      posts: []
    }
  },
  async created() {
    const response = await axios.get('https://raw.githubusercontent.com/nfl0/webdata/master/activities/activities.json')
    this.posts = response.data
  },
  head () {
    return {
      title: "Activités - Association Akal N'tine Dartanout",
      meta: [
        { hid: 'description', name: 'description', content: "Activities and Events conducted by Association Akal N'tine Dartanout Association" }
      ]
    }
  }
}
</script>

<style lang="scss">
.activities-page{
  .activity-image {
    .progressive-image-wrapper,
    .progressive-image-main,
    .progressive-image-placeholder {
      max-width: inherit!important;
      padding: 0 !important;
    }
  }
  .card-image {
    img {
      width: 100%;
      object-fit: cover;
      height: 250px;
    }
  }

  .page-title {
    color: black;
    font: Bold 40px/43px Source Sans Pro;
  }
  .activity-card {
    text-align: center;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    cursor: pointer;
    border-radius: 8px;
    padding: 10px;
    max-width: 450px;
    height: auto;
  }
  .activity-card:hover {
    transform: scale(0.98, 0.99);
      box-shadow: 0 0 10px rgb(88, 90, 90);
    transition: 0.3s;
  }
  .act-card-title {
    color: #035f59;
  }
  .act-card-date {
    color: rgb(49, 49, 49);
    font-weight: 700;
  }
  .activities-wrapper{margin: 0 auto;}
  @media screen and (min-width: 600px) {
    .activity-card {height: 420px;}
  }
}
</style>