<template>
  <div id="faq">
    <li>
      <label htmlFor="{{ for }}">
        {{ title }}
        <span className="faq_icon">
          <i class="fa-solid fa-chevron-down"></i>
        </span>
      </label>
      <input type="radio" name="pricing" id="{{ id }}" />
      <div className="content">
        <p>{{ content_1 }}</p>
        <p>{{ content_2 }}</p>
        <p>{{ content_3 }}</p>
        <p>{{ content_4 }}</p>
      </div>
    </li>
  </div>
</template>

<script>
export default {
  name: "Accordion_item",
  props: {
    for: String,
    id: String,
    title: String,
    content_1: String,
    content_2: String,
    content_3: String,
    content_4: String,
  },
};
</script>

<style scoped>
@media (min-width: 0) {
  #faq {
    padding: 0;
    color: black;
    /* background-color: var(--dark-light-accent); */
    background-color: red;
    margin: 100px auto;
    width: 100%;
  }

  li {
    list-style: none;
  }

  li label {
    font-family: var(--ff-secondary);
    /* background-color: rgb(240, 200, 200); */
    border-bottom: 2px solid rgb(193, 193, 193);
    width: 100%;
    cursor: pointer;
    padding: 1.5rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    /* font-weight: 900; */
    transition: var(--transition);
  }

  li label:hover {
    background-color: var(--dark-accent);
    color: var(--white);
  }

  label + input[type="radio"] {
    display: none;
  }

  .content {
    padding: 0 var(--rem);
    line-height: 26px;
    max-height: 0;
    overflow: hidden;
    transition: var(--transition);
    background-color: rgb(234, 232, 232);
    color: #000000;
  }

  label + input[type="radio"]:checked + .content {
    max-height: 500px;
  }
}

@media (min-width: 1025px) {
}

@media (min-width: 600px) {
}
</style>
