<template>
  <section class="featured_section">
    <div class="featured_container">
      <span class="featured_text">
        <h1>Full Selectric speed ahead</h1>
        <p>
          Audi recently underpinned its clear course toward electromobility with
          strong figures and important milestones. How the Four Rings are
          progressing on their path to successful electrification.
        </p>

        <button>Read More</button>
        <span class="sup_text"
          ><sup>1</sup
          ><small
            >The vehicle shown is a concept that is not available as a
            production vehicle.</small
          ></span
        >
      </span>
      <picture>
        <img
          src="https://www.progress.audi/content/dam/progress/story/2021/wow-audi-grandsphere-concept/1920x1080-desktop-M21-Audi-grandsphere-concept-09821B01.jpg?imwidth=1920&imdensity=1"
          alt="An AUDI concept car"
        />
      </picture>
    </div>
  </section>
</template>

<script>
export default {
  name: "Featured_one",
};
</script>

<style scoped>
@media (min-width: 0) {
  /* Main containers */
  .featured_section {
    display: block;
    padding: var(--padding-min);
    height: 100vh;
    display: flex;
    align-items: center;
  }

  .featured_container {
    display: flex;
    gap: 1rem;
    align-items: center;
    height: fit-content;
    flex-direction: column;
  }

  /* Text section */
  .featured_text {
    flex: 40%;
    order: 2;
    display: flex;
    gap: 1.5rem;
    flex-direction: column;
    align-items: start;
  }

  button {
    cursor: pointer;
    color: var(--dark);
    background: transparent;
    border: var(--border-px);
    padding: var(--btn-padding);
    transition: var(--transition);
    font-family: var(--ff-primary);
  }

  button:hover {
    color: var(--dark-accent);
  }

  .sup_text {
    display: flex;
  }

  sup {
    font-size: 10px;
  }

  small {
    font-size: var(--fs-small);
  }

  /* Image section */

  picture {
    order: 1;
    height: 100%;
    width: 100%;
    flex: 60%;
    object-fit: cover;
  }

  img {
    width: 100%;
    height: 100%;
  }
}

@media (min-width: 1025px) {
  .featured_container {
    flex-direction: row;
    height: 70%;
  }

  picture {
    order: 2;
  }

  .featured_text {
    order: 1;
  }
}

@media (min-width: 1240px) {
  .featured_section {
    padding: 2rem var(--px);
  }
}
</style>
