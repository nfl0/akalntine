<template>
  <section class="activities-page">
    <h1 class="page-title center-align">
      Activities
    </h1>
    <div class="container activities-wrapper">
      <div class="row">
        <div class="col s12 m6">
          <div class="card activity-card">
            <iframe src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2Fasso.akalntine%2F&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"></iframe>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.activities-page {
  height: 100vh; /* Set the section height to fill the viewport */
  display: flex; /* Use flexbox to align items */
  flex-direction: column; /* Arrange items vertically */
  justify-content: center; /* Center items vertically */
  align-items: center; /* Center items horizontally */

  .activity-card {
    text-align: center;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    cursor: pointer;
    border-radius: 8px;
    padding: 10px;
    max-width: 450px;
    height: 100%; /* Make the card fill the section height */
  }

  .page-title {
    color: black;
    font: Bold 40px/43px Source Sans Pro;
  }

  .activities-wrapper {
    margin: 0 auto;
    height: 100%; /* Make the wrapper fill the card height */
  }
}
</style>
