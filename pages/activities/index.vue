<template>
  <section class="activities-page">
    <h1 class="page-title center-align">
      Activités
    </h1>
    <div class="container activities-wrapper">
      <div class="row">
        <div class="col s12">
          <div class="fb-page" data-href="https://www.facebook.com/asso.akalntine" data-tabs="timeline" data-width="500" data-height="500" data-small-header="false" data-adapt-container-width="true" data-hide-cover="false" data-show-facepile="true">
            <blockquote cite="https://www.facebook.com/asso.akalntine" class="fb-xfbml-parse-ignore">
              <a href="https://www.facebook.com/asso.akalntine">Association Akal N'tine Dartanout</a>
            </blockquote>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  head() {
    return {
      title: 'Activités - Association Akal N\'tine Dartanout',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Activities and Events conducted by Association Akal N\'tine Dartanout Association',
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.activities-page {
  .page-title {
    color: black;
    font: bold 40px/1.1 'Source Sans Pro', sans-serif;
    margin-bottom: 2rem;
  }
  .activities-wrapper {
    margin: 0 auto;
  }
  .fb-page {
    width: 100%;
    overflow: hidden;
    border: none;
  }
}
</style>
