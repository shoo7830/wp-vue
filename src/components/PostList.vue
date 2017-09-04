<template>
  <div>
  <ul v-if="postlists.length">
    <li v-for="postlist in postlists">
      <p v-for="url in postlist.attachments"><img :src="url.url"></p>
      <p><a :href="postlist.url" target="_blank" rel="noopener">{{ postlist.title_plain }}</a></p>
      <div v-html="postlist.content"  class="post-content"></div>
      <p><a :href="postlist.url" target="_blank" rel="noopener">더보기</a></p>
    </li>
  </ul>
  </div>
</template>
<script>

import 'expose-loader?$!expose-loader?jQuery!jquery'
export default {
  name: 'post-list',
  data: function () {
   return {
      postlists: []
    }
  },

  mounted: function () {
    var self = this;
    $.ajax({
      url: 'http://webholic.net/api/get_recent_posts/?count=4',
      method: 'GET',
      success: function (response) {
          self.postlists = response.posts
      },
      error: function (error) {
          alert(JSON.stringify(error))
      }
    })
  }
}

</script>

<style lang="scss">
h1, h2, h3, h4, h5, h6 {font-size: 16px}
h2 {
  font-weight: normal;
}
ul {
  &:after {
    display: block;
    content: '';
    clear: both;
  }

  li {
    margin: 0;
    padding: 0;
    list-style: none;
    float: left;
    width: 25%;
  }
}

.post {
  margin: 0;
  padding: 0;

  h2 {
    font-weight: normal;
    //font-size: 14px;
  }
}

.post-content {
  height:208px;
  overflow: hidden;
}
</style>
