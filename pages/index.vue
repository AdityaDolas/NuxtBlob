<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :excerpt="post.git1"
      :thumbnailImage="post.thumbnailUrl"
      :id="post.id"
    />
  </section>
</template>

<script>
import axios from 'axios';
import PostPreview from "@/components/Blog/PostPreview";
export default {
  components: {
    PostPreview
  },
  data() {
    return {
      students: null,
      posts: [
        {
          title: "Top 10 git Commands",
          previewText: "hi",
          git1: "1 - git init",
          thumbnailUrl:
            "https://github.blog/wp-content/uploads/2020/03/git-2-26.png?fit=1200%2C630",
          id: "a-new-beginning"
        }
      ]
    };
  },
  created: function () {
			this.fetchApi();
		},
		methods: {
			fetchApi: function () {
				var url = 'http://localhost:8080/api/students';
				axios.get(url)
					.then(function (res) {
            this.students = res.data;
            console.log(this.students);
					})
			}
		}
};
</script>

<style scoped>
#posts {
  padding-top: 0rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>