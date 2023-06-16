<template>
  <section class="activities-page">
    <h1 class="page-title center-align">
      Activités
    </h1>
    <div class="container activities-wrapper">
      <div class="row">
        <div class="col s12">
          <div class="iframe-wrapper">
            <div
              class="fb-page"
              data-width="10000"
              data-adapt-container-width="true"
              data-href="https://www.facebook.com/asso.akalntine"
              data-tabs="timeline"
              data-small-header="false"
              data-hide-cover="false"
              data-show-facepile="true"
            ></div>
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
      title: "Activités - Association Akal N'tine Dartanout",
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: "Activities and Events conducted by Association Akal N'tine Dartanout Association",
        },
      ],
    };
  },
  mounted() {
    const TIMEOUT = null;
    window.addEventListener('resize', () => {
      if (TIMEOUT === null) {
        window.setTimeout(() => {
          $('.fb-page').removeClass('fb_iframe_widget fb_iframe_widget_fluid');
          FB.XFBML.parse();
        }, 300);
      }
    });
  },
};
</script>

<style lang="scss">
.activities-page {
  .page-title {
    color: black;
    font: bold 40px/1.1 "Source Sans Pro", sans-serif;
    margin-bottom: 2rem;
  }
  .activities-wrapper {
    margin: 0 auto;
  }
  .iframe-wrapper {
    position: relative;
    height: 0;
    padding-bottom: 56.25%; /* 16:9 aspect ratio */
    overflow: hidden;
  }
  iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: none;
    overflow: hidden;
  }
}
</style>
