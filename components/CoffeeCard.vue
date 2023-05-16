<template>
  <div class="coffee-card">
    <div class="flex-none">
      <h2>{{ title }}</h2>
      <img :src="image" :alt="altText" class="coffee-image float" />
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },
    altText: {
      type: String,
      default: "Coffee Image",
    },
    description: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.coffee-card {
  border: 1px solid #ccc;
  padding: 16px;
  border-radius: 10px;
  margin-bottom: 16px;
  float: left;
}
img {
  float: left;
  margin-right: 1rem;
}
.coffee-image {
  width: 300px;
  height: 200px;
  object-fit: cover;
  border-radius: 8px;
}
title {
  float: left;
}
</style>
