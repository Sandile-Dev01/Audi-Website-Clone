<template>
  <section class="featured_section">
    <div class="featured_container">
      <picture>
        <img
          src="https://www.audi.com/content/dam/gbp2/career-n/Working-at-Audi/Arbeitgeberkampagne_2023/1920x1080_T4_Tiantian_DSC09637.jpg?imwidth=792&imdensity=1"
          alt=""
        />
      </picture>
      <span class="featured_text">
        <h1>#WorkingInProgres</h1>
        <p>
          Help us to design the mobility of tomorrow. With cars that use
          state-of-the-art technology to offer an awesome driving experience
          and, at the same time, pave the way into a future that is digital,
          sustainable and electric.
        </p>

        <button>Read More</button>
      </span>
    </div>
  </section>
</template>

<script>
export default {
  name: "Featured_two",
};
</script>

<style scoped>
@media (min-width: 0) {
  /* Main containers */
  .featured_section {
    display: block;
    padding: var(--padding-min);
    height: 80vh;
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
    height: 90%;
  }
}

@media (min-width: 1240px) {
  .featured_section {
    padding: 2rem var(--px);
  }
}
</style>
