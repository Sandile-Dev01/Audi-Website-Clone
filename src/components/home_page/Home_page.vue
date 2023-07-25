<template>
  <div class="home_page_container">
    <div class="layout"></div>
    <div class="home_img"></div>

    <span class="home_text">
      <h1>Audi Social Day</h1>
      <p>Around 1,000 Audi employees got involved for a good cause</p>
      <button>Learn more</button></span
    >
  </div>
</template>

<script>
export default {
  name: "Home_page",
};
</script>

<style scoped>
@media (min-width: 0) {
  .home_page_container {
    display: block;
    position: relative;
    font-size: calc(var(--rem) * 2);
    text-align: center;
    color: var(--light);
    height: 65vh;
    overflow: hidden;
  }

  .layout {
    display: none;
    transition: var(--transition);
  }

  .layout:hover {
    display: inline;
  }

  .home_img {
    position: absolute;
    z-index: 1;
    height: 100%;
    width: 100%;
    overflow: hidden;
    background: url("https://www.audi.com/content/dam/gbp2/2023/Homepage/Stage/1920x600_Social-Day_04A1394-02.jpg?imwidth=1920&imdensity=1");
    background-size: cover;
    background-repeat: no-repeat;
    transition: all 450ms ease-in-out;
  }

  .home_page_container:hover .home_img {
    scale: 1.1;
  }

  .home_page_container:hover .layout {
    overflow: hidden;
    background-color: var(--layout);
    position: absolute;
    top: 0;
    left: 0;
    z-index: 4;
    width: 100%;
    min-height: 100%;
    display: inline;
  }

  .home_text {
    position: absolute;
    z-index: 5;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    width: 100%;
    display: flex;
    gap: 1.5rem;
    flex-direction: column;
    align-items: center;
  }

  .home_text h1 {
    font-size: 10vw;
  }

  .home_text p,
  button {
    display: none;
  }
}

@media (min-width: 768px) {
  .home_text h1 {
    font-size: 2.5ch;
  }
}

@media (min-width: 1280px) {
  .topics_text {
    display: none;
  }

  .home_text p,
  button {
    display: inline;
  }

  button {
    cursor: pointer;
    border: 1px solid var(--light);
    color: var(--light);
    background: transparent;
    padding: var(--btn-padding);
    transition: var(--transition);
    font-family: var(--ff-primary);
  }

  button:hover {
    border: 1px solid var(--light-accent);
    color: var(--light-accent);
  }
}
</style>
