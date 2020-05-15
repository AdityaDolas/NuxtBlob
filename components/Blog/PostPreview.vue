<template>
  <nuxt-link
    :to="id">
    <article class="post-preview">
      <div
        :style="{backgroundImage: 'url(' + thumbnailImage + ')'}"
        class="post-preview-thumbnail"></div>
      <div class="post-preview-content">
        <h1>{{ title }}</h1>
        <p>{{ excerpt }}</p>
        <p>{{git2}}</p>
        <p>{{git3}}</p>
        <p>{{git4}}</p>
        <p>{{git5}}</p>
        <p>{{git6}}</p>
        <p>{{git7}}</p>
        <p>{{git8}}</p>
        <p>{{git9}}</p>
        <p>{{git10}}</p>
      </div>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    excerpt: {
      type: String,
      required: true
    },
    git2:{
        type: String,
        required: true
    },
    git3:{
        type: String,
        required: true
    },
    git4:{
        type: String,
        required: true
    },
    git5:{
        type: String,
        required: true
    },
    git6:{
        type: String,
        required: true
    },
    git7:{
        type: String,
        required: true
    },
    git8:{
        type: String,
        required: true
    },
    git9:{
        type: String,
        required: true
    },
    git10:{
        type: String,
        required: true
    },
    thumbnailImage: {
      type: String,
      required: true
    },
    id: {
      type: String,
      required: true
    }
  }
};
</script>

<style scoped>
a {
  text-decoration: none;
  color: black;
}
.post-preview {
  border-radius: 3px;
  box-shadow: 1px 1px 5px 1px rgba(0, 0, 0, 0.5);
  width: 90%;
  height: 33rem;
  margin: 1rem;
}
.post-preview-thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 5rem;
}
.post-preview-content {
  text-align: left;
  padding: 1rem;
}
@media (min-width: 35rem) {
  .post-preview {
    width: 25rem;
  }
}
</style>