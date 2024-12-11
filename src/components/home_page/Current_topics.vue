<template>
  <div class="topics_item">
    <div class="home_img">
      <div class="layout"></div>

      <img :src="image" alt="IMG" />
    </div>

    <p class="sub_title">{{ sub_title }}</p>
    <h2>{{ title }}</h2>
    <p>
      {{ text }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Current_topics",

  props: {
    image: String,
    title: String,
    sub_title: String,
    text: String,
  },
};
</script>

<style scoped>
@media (min-width: 0) {
  .topics_item {
    cursor: pointer;
  }

  .sub_title {
    color: var(--dark-accent);
    letter-spacing: 1.5px;
    font-size: 0.8rem;
    padding-top: 0.25rem;
  }

  .home_img {
    width: 100%;
    height: 60%;
    object-fit: cover;
    position: relative;
    overflow: hidden;
  }

  img {
    width: 100%;
    height: 100%;
    overflow: hidden;
    transition: var(--transition-1);
  }

  .layout {
    display: none;
  }

  .topics_item:hover img {
    scale: 1.2;
  }

  .topics_item:hover .layout {
    display: inline;
    overflow: hidden;
    position: absolute;
    z-index: 1;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    padding: 5rem;
    background-color: var(--layout);
  }
}
</style>
