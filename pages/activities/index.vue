<template>
  <section class="activities-page">
    <h1 class="page-title">Activities</h1>
    <div class="container activities-wrapper">
      <div class="row">
        <div class="col s12 m6">
          <div class="card activity-card">
            <div class="iframe-wrapper">
              <iframe
                src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2Fasso.akalntine%2F&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId"
                frameborder="0"
                allowfullscreen="true"
                allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
              ></iframe>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.activities-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.page-title {
  color: black;
  font-weight: bold;
  font-size: 40px;
  line-height: 43px;
}

.activity-card {
  text-align: center;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  cursor: pointer;
  border-radius: 8px;
  padding: 10px;
  max-width: 450px;
  height: 100%;
}

.iframe-wrapper {
  height: 100%;
}

iframe {
  width: 100%;
  height: 100%;
  border: none;
}
</style>
