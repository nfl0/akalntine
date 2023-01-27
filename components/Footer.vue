<template>
  <footer class="page-footer #37474f blue-grey darken-3">
    <div class="container">
      <div class="row ">
        <div class="col l6 s12">
          <h5 class="white-text">
            Navigation
          </h5>
          <ul>
            <li>
              <nuxt-link to="/" class="grey-text text-lighten-3">
                Page d'accueil
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/newsletter" class="grey-text text-lighten-3">
                Bulletin
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/gallery" class="grey-text text-lighten-3">
                Galerie
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/blog" class="grey-text text-lighten-3">
                Blog
              </nuxt-link>
            </li>
          </ul>
        </div>
        <div class="col l4 offset-l2 s12">
          <h5 class="white-text">
            Liens
          </h5>
          <ul>
            <li>
              <a href="https://www.communesmaroc.com/commune/tanalt" class="grey-text text-lighten-3">
                Tanalt
              </a>
            </li>
            <li>
              <a href="https://www.youtube.com/@associationakalntine6207/videos" class="grey-text text-lighten-3">
                YouTube
              </a>
            </li>
            <li>
              <a href="https://github.com/stacsnssce/official-website" class="grey-text text-lighten-3">
                Code Source
              </a>
            </li>
            <li>
              <a href="/contributors" class="grey-text text-lighten-3">
                Contributeurs
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-copyright #263238 blue-grey darken-4">
      <div class="container center">
        Akal Ntine Dartanout © 2023
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
li {
  font-size: 18px;
}

.footer-copyright {
  font-size: 16px;
  font-weight: 600;
}

h5 {
  font-size: 28px;
  font-weight: 600;
  text-decoration: underline;
}
</style>
