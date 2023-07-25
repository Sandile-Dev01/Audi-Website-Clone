<template>
  <div class="footer_links">
    <h2>{{ header }}</h2>

    <span
      ><p>{{ link_item_1 }}</p>
      <p>{{ link_item_2 }}</p>
      <p>{{ link_item_3 }}</p>
      <p>{{ link_item_4 }}</p></span
    >
  </div>
</template>

<script>
export default {
  name: "Footer_links",
  props: {
    header: String,
    link_item_1: String,
    link_item_2: String,
    link_item_3: String,
    link_item_4: String,
  },
};
</script>

<style scoped>
h2 {
  margin-bottom: calc(var(--rem) * 2);
}

span {
  display: flex;
  flex-direction: column;
  gap: calc(var(--rem) * 1.6);
}

p {
  transition: var(--transition);
  cursor: pointer;
  font-size: 0.75rem;
  letter-spacing: 1.5px;
  font-weight: bold;
}

p:hover {
  color: var(--dark-accent);
}
</style>
