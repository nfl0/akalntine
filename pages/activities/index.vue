<template>
  <section class="activities-page">
    <h1 class="page-title center-align">
      Activités
    </h1>
    <div class="container activities-wrapper">
      <div class="row">
        <div class="col s12">
          <iframe
            src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2Fasso.akalntine&tabs=timeline&width=500&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId"
            width="500"
            height="500"
            style="border:none;overflow:hidden"
            scrolling="no"
            frameborder="0"
            allowfullscreen="true"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
          ></iframe>
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
    font: Bold 40px/43px Source Sans Pro;
  }
  .activities-wrapper {
    margin: 0 auto;
  }
}
</style>
