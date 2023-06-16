<template>
  <section class="activities-page">
    <h1 class="page-title center-align">
      Activités
    </h1>
    <div class="container activities-wrapper">
      <div class="row">
        <div class="col s12">
          <div v-if="posts.length > 0" class="facebook-posts">
            <div v-for="post in posts" :key="post.id" class="post">
              <div v-html="post.message"></div>
              <!-- Render other post details as needed -->
            </div>
          </div>
          <div v-else class="no-posts-message">
            No posts available.
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      posts: [],
    };
  },
  async mounted() {
    await this.fetchFacebookPosts();
  },
  methods: {
    async fetchFacebookPosts() {
      try {
        const response = await fetch(
          'https://graph.facebook.com/v13.0/1336162506510924/posts?fields=message&access_token=YOUR_ACCESS_TOKEN'
        );
        const data = await response.json();
        this.posts = data.data;
      } catch (error) {
        console.error('Error fetching Facebook posts:', error);
      }
    },
  },
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
  .facebook-posts {
    // Adjust the styling for your Facebook posts
  }
  .post {
    // Adjust the styling for each Facebook post
  }
  .no-posts-message {
    // Adjust the styling for the message when no posts are available
  }
}
</style>
