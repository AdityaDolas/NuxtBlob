<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :excerpt="post.git1"
      :git2="post.git2"
      :git3="post.git3"
      :git4="post.git4"
      :git5="post.git5"
      :git6="post.git6"
      :git7="post.git7"
      :git8="post.git8"
      :git9="post.git9"
      :git10="post.git10"
      :thumbnailImage="post.thumbnailUrl"
      :id="post.id"

    />
  </section>
</template>

<script>
import PostPreview from "@/components/Blog/PostPreview";
export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: "Top 10 git Commands",
          previewText: "hi",
          git1: "1 - git init",
          git2: "2 - git add .",
          git3: '3 - git commit -m "FC"',
          git4: "4 - git stash",
          git5: "5 - git stash pop",
          git6: "6 - git log --oneline",
          git7: "7 - git merge",
          git8: "8 - git branch",
          git9: "9 - git checkout",
          git10: "10 - git checkout -b branch_name",
          thumbnailUrl:
            "https://github.blog/wp-content/uploads/2020/03/git-2-26.png?fit=1200%2C630",
          id: "a-new-beginning"
        }
      ]
    };
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