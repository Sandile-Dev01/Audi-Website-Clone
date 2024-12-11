<template>
  <div class="home_container">
    <div class="img_container">
      <img
        src="https://www.audi.com/content/dam/gbp2/models/1920x1080-desktop-models-teaser-q4_ed1_2021_2543.jpg?imwidth=792&imdensity=1"
        alt="Audi Cars"
      />
    </div>
    <div class="text_container">
      <h3>At Audi you’ll find the right vehicle for every requirement</h3>
      <p>
        Sporty, luxurious, or compact – at Audi you will find the right vehicle
        for every requirement. Discover and configure our series models now.
      </p>
      <button>Discover all models</button>

      <small
        >Audi Q4 Sportback e-tron:Power consumption (combined*) in kWh/100 km:
        19.7–16.1CO₂ emissions (combined*) in g/km: 0</small
      >
      <small
        >Information on fuel/power consumption and CO₂ emissions with ranges
        depending on the selected equipment of the vehicle.</small
      >
      <small>
        Only consumption and emission values according to WLTP and not according
        to NEDC are available for the vehicle.
      </small>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home_last",
};
</script>

<style scoped>
@media (min-width: 0) {
  .home_container {
    background-color: #fff;
    display: block;
    position: relative;
    z-index: 20;
    display: flex;
    flex-direction: column;

    padding: calc(var(--rem) * 4) calc(var(--rem) * 1.8) var(--px);
    align-items: center;
    gap: calc(var(--rem) + var(--half-rem));
  }

  small {
    font-size: var(--fs-small);
  }

  .img_container {
    object-fit: cover;
    width: 100%;
  }

  .img_container img {
    width: 100%;
  }
  .text_container {
    display: flex;
    flex-direction: column;
    gap: var(--rem);
    /* justify-content: space-evenly; */
  }

  button {
    color: var(--dark);
    font-family: var(--ff-primary);
    background: transparent;
    border: var(--border-px);
    padding: var(--btn-padding);
    cursor: pointer;
    font-size: 1.4ch;
    transition: var(--transition);
  }

  button:hover {
    color: var(--dark-accent);
  }
}

@media (min-width: 1000px) {
  .home_container {
    padding: var(--px);
    flex-direction: row;
  }

  button {
    width: fit-content;
  }
}
</style>
