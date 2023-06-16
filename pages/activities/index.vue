<template>
  <section class="activities-page">
    <h1 class="page-title center-align">
      Activités
    </h1>
    <div class="container activities-wrapper">
      <div class="row">
        <div class="col s12">
          <div class="iframe-wrapper">
            <iframe
              src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2Fasso.akalntine&tabs=timeline&width=500&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId"
              frameborder="0"
              allowfullscreen="true"
              allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
            ></iframe>
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
