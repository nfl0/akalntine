<template>
  <section class="activities-page">
    <h1 class="page-title center-align">
      Activities
    </h1>
    <div class="container activities-wrapper">
      <div class="row">
        <div class="col s12 m6">
          <div class="card activity-card">
            <iframe src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2Fasso.akalntine%2F&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId" width="100%" height="100vh" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"></iframe>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from 'axios'
const fm = require('front-matter')

export default {
  // ...
}
</script>

<style lang="scss">
.activities-page {
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
  .page-title {
    color: black;
    font: Bold 40px/43px Source Sans Pro;
  }
  .activities-wrapper {
    margin: 0 auto;
  }
  @media screen and (min-width: 600px) {
    .activity-card {
      height: 420px;
    }
  }
}
</style>
