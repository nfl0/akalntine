<template>
  <section class="post-wrapper card container">
    <h1 class="page-title center-align">
      Blog Posts
    </h1>
    <div class="container">
      <div v-for="post in posts.slice().reverse()" :key="post.id" class="row blog-card">
        <div class="col blog-col s12 m3 l4 center-align hide-on-med-and-up">
          <progressive-img
            :src="`${post.attribute.image}`"
            :placeholder="`/imageplaceholder1x1.png`"
            blur="30"
            delay="200"
            class="blog-image center-align"
          />
        </div>
        <div class="col l8 blog-card-content">
          <h3 class="blog-title">
            {{ post.attribute.title }}
          </h3>
          <h5 class="blog-desc">
            {{ post.attribute.desc }}
          </h5>
          <div class="author">
            <div class="author-image">
              <img :src="`https://github.com/${post.attribute.author}.png?size=50`" alt="">
            </div>
            <div class="author-details">
              <h5 class="author-name">
                <i class="material-icons">create</i> {{ post.attribute.name }}
              </h5>
              <h5 class="blog-date">
                <i class="material-icons">date_range</i> {{ post.attribute.date }}
              </h5>
            </div>
          </div>
          <nuxt-link :to="{name: 'blog-slug', params:{slug: post.slug, id: post.id}}">
            En savoir plus....
          </nuxt-link>
        </div>
        <div class="col blog-col s12 m3 l4 center-align hide-on-small-only ">
          <progressive-img
            :src="`${post.attribute.image}`"
            :placeholder="`/imageplaceholder1x1.png`"
            blur="30"
            delay="200"
            class="blog-image center-align"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from 'axios'
const fm = require('front-matter')

export default {
  fetch ({ store }) {
    // const psts = []
    return axios.get('https://api.github.com/repos/nfl0/webdata/contents/posts')
      .then(async ({ data }) => {
        /* eslint-disable no-console */
        store.commit('blogPosts', await Promise.all(data.map(async (element) => {
          return await axios.get(element.download_url)
            .then((res) => {
              const mdf = fm(res.data)
              // eslint-disable-next-line
              // console.log(mdf)
              return {
                attribute: mdf.attributes,
                slug: element.sha,
                body: mdf.body,
                id: element.name.slice(0, -3)
              }
            })
            // store.commit('blogPosts', psts)
        })))
      })
      .then(() => {
      })
  },
  computed: {
    posts () {
      return this.$store.state.posts
    }
  },
  // async asyncData (context) {
  // }
  head () {
    return {
      title: 'Blog Posts - STACS',
      meta: [
        { hid: 'description', name: 'description', content: 'Here is the Blogs and thoughts shared by students of Department of Computer Science and Engineering' }
      ]
    }
  }
}
</script>

<style lang="scss">
.post-wrapper {
  margin: 12px auto;
  padding: 20px 0;

  .page-title {
    font-size: 32px;
    font-weight: bolder;
    font: Bolder 40px/43px Source Sans Pro;
  }
  .blog-card {
    padding: 20px;
    cursor: pointer;
    box-shadow: 0 0 10px rgba(100, 100, 100,0.5);
    transition: 0.2s linear;
    border-radius: 8px;
    transform: scale(1.01);
    background-color: white;

    &:hover {
      transform: scale(1);
      box-shadow: 0 0 10px rgba(100, 100, 100,0.2);
    }
    .blog-col {
      padding: 0 !important;

      .blog-image {
        max-width: 180px !important;
        width: 180px !important;
        height: 180px !important;
        padding: 0 !important;

        * {
          padding: 0 !important;
        }

        .progressive-image-wrapper,
        .progressive-image-main,
        .progressive-image-placeholder {
          width: 180px!important;
          height: 180px!important;
          padding: 0 !important;
        }
        img {
          object-fit: cover;
        }
      }
    }

    .blog-card-content{
      .blog-title {
        font-size: 24px;
        font-weight: bold;
        padding-bottom: 12px;
        border-bottom: solid 1px #057e6e;
      }
      .author {
        display: flex;

        .author-image {
          margin-right: 12px;
          width: 50px;
          height: 50px;
          object-fit: cover;
          border-radius: 50%;
          overflow: hidden;
        }
        .author-details {
          padding-top: 4px;

          .author-name {
            font-size: 16px;
            font-weight: bold;
            margin: 0 !important;

            i {
              margin-right: 8px;
              font-size: 16px;
              line-height: 12px;
            }
          }
        }
      }
      .blog-date{
        font-size: 16px;
        margin: 12px 0!important;

        i {
          margin-right: 8px;
          font-size: 16px;
          line-height: 12px;
        }
      }
      .blog-desc {
        margin: 12px 0!important;
        font-size: 18px;
        font-weight: 600;
        color: gray;
      }
      a {
        margin-bottom: 20px;
      }
    }
  }
}
</style>
