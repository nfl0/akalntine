<template>
  <section class="activities-page">
    <h1 class="page-title center-align">
      Activités
    </h1>
    <div class="container activities-wrapper">
      <div class="row">
        <div class="col s12">
          <div class="fb-page center-block" data-width="10000" data-adapt-container-width="true" data-href="https://www.facebook.com/asso.akalntine"></div>
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
    // Load Facebook SDK
    (function(d, s, id) {
      var js, fjs = d.getElementsByTagName(s)[0];
      if (d.getElementById(id)) return;
      js = d.createElement(s); js.id = id;
      js.src = "https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v10.0";
      fjs.parentNode.insertBefore(js, fjs);
    }(document, 'script', 'facebook-jssdk'));
  },
};
</script>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>

<script>
  var TIMEOUT = null;

  $(window).on('resize', function() {
    if (TIMEOUT === null) {
      TIMEOUT = window.setTimeout(function() {
        TIMEOUT = null;
        // fb_iframe_widget class is added after first FB.FXBML.parse()
        // fb_iframe_widget_fluid is added in the same situation, but only for mobile devices (tablets, phones)
        // By removing those classes FB.XFBML.parse() will reset the plugin widths.
        $('.fb-page').removeClass('fb_iframe_widget fb_iframe_widget_fluid');

        FB.XFBML.parse();
      }, 300);
    }
  });
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
}
</style>
