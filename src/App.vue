<template>
  <header>
    <Navbar />
    <Home_page />
    <div class="topics_container">
      <span class="topics_text">
        <p>Around 1,000 Audi employees got involved for a good cause</p>
        <button>Learn more</button></span
      >

      <h1>Current topics in the world of Audi</h1>
    </div>
    <div class="topics">
      <Current_topics
        image="https://www.audi.com/content/dam/gbp2/career/experienced-professionals/Fertigungsfachkraft/1920x1080_A227176_large.jpg?imwidth=477&imdensity=1"
        sub_title="Experienced Professionals"
        title="Production specialists in assembly"
        text="We are looking for production specialists in series production for the
    start-up of the new vehicle models at the Ingolstadt side. Interested ?
    Then apply for the Ingolstadt site!"
      />
      <Current_topics
        image="https://www.audi.com/content/dam/gbp2/innovation/development/rear-lights/1920x1080_A191488_medium.jpg?imwidth=477&imdensity=1"
        sub_title="Digitalization - 05/12/2023"
        title="Light : At the heart of Audi's DNA"
        text="Audi is revolutionizing light design with digital OLED rear lights. The innovative technology how the car communicates with its environment"
      />
      <Current_topics
        image="https://robbreport.com/wp-content/uploads/2021/03/audiicengines.jpg?w=1000"
        sub_title="Value Creation & Production - 03/16/2023"
        title="Back to a new life"
        text="Does the circular economy in the automotive industry work in practice as well as in theory?
         Audi is attempting to find this out and is testing how to close as many material cycles on balance as 
         possible in the MaterialLoop project involving 100 used vehicles."
      />
    </div>

    <Featured_one />
    <Featured_two />

    <div class="topics_container">
      <h1>Press releases</h1>
    </div>

    <div class="topics">
      <Press_releases
        image="https://www.audi.com/content/dam/gbp2/2023/Homepage/Pressemitteilungen/1920x1080_A233591_large.jpg?imwidth=477&imdensity=1"
        sub_title=" - 07/12/2023"
        title="Trainee project at Audi Neckarsulm: NSU Prinz with e-tron power"
      />
      <Press_releases
        image="https://www.audi.com/content/dam/gbp2/2023/Homepage/Pressemitteilungen/1920x1080_A233576_large.jpg?imwidth=477&imdensity=1"
        sub_title=" - 07/06/2023"
        title="Audi creates 500 new electric mobility jobs at its Ingolstadt location"
      />
      <Press_releases
        image="https://www.audi.com/content/dam/gbp2/2023/Homepage/Pressemitteilungen/1920x1080_A233164_large.jpg?imwidth=477&imdensity=1"
        sub_title="- 06/29/2023"
        title="Gernot Döllner named as new Audi CEO"
      />
    </div>

    <div class="media_button_container">
      <button>To the Audi MediaCenter</button>
    </div>

    <Home_last_section />
    <Footer />
  </header>
</template>

<script>
import Navbar from "./components/navbar/Navbar.vue";
import Home_page from "./components/home_page/Home_page.vue";
import Current_topics from "./components/home_page/Current_topics.vue";
import Featured_one from "./components/home_page/Featured_one.vue";
import Featured_two from "./components/home_page/Featured_two.vue";
import Press_releases from "./components/home_page/Press_releases.vue";
import Home_last_section from "./components/home_page/Home_last_section.vue";
import Footer from "./components/footer/Footer.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Home_page,
    Current_topics,
    Featured_one,
    Featured_two,
    Press_releases,
    Home_last_section,
    Footer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@100;400&display=swap");

*,
html {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  font-family: "Montserrat", sans-serif;
}

input {
  border-radius: 0;
}

h1,
h2,
h3 {
  letter-spacing: 2px;
}

:root {
  --dark: #000000;
  --dark-accent: #9b9898;
  --darker-accent: #1a1616;

  --light: #ffffff;
  --light-accent: #ded2d2;

  --layout: rgba(0, 0, 0, 0.3);
  --padding-min: var(--rem) calc(var(--rem) * 1.8);

  --fs-small: 12px;
  --rem: 1rem;
  --half-rem: 0.5rem;
  --px: 6.5rem;
  --btn-padding: 1.15rem 5rem;
  --border-px: 1px solid var(--dark);

  --bolder: bolder;

  --transition: all 250ms ease-in-out;
  --transition-1: all 450ms ease-in-out;
}

@media (min-width: 0) {
  .topics_container {
    padding: calc(var(--rem) * 3) 0 var(--rem);
  }

  .topics_container h1 {
    text-align: center;
    font-size: 1.2rem;
    padding: var(--padding-min);
  }

  .topics {
    padding: var(--padding-min);
    display: grid;
    gap: calc(var(--rem) * 2);
    grid-template-columns: 1fr;
  }

  .topics_text {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: calc(var(--rem) * 2);
    margin-bottom: calc(var(--rem) * 6);
  }

  .topics_text p {
    font-size: 2.4vw;
  }

  .topics_text button {
    font-family: var(--ff-primary);
    cursor: pointer;
    border: 1px solid var(--dark);
    color: var(--dark);
    background: transparent;
    padding: 1rem 5rem;
    transition: var(--transition);
  }

  .topics_text button:hover {
    color: var(--dark-accent);
  }

  /* black media center button styles */

  .media_button_container {
    margin-top: var(--px);
    display: flex;
    justify-content: center;
    padding: var(--padding-min);
  }

  .media_button_container button {
    cursor: pointer;
    font-weight: var(--bolder);
    padding: var(--btn-padding);
    border: none;
    background-color: var(--dark);
    color: var(--light);
    font-family: var(--ff-primary);
    font-size: 2vw;
    transition: var(--transition);
    width: 100%;
  }

  .media_button_container button:hover {
    opacity: 0.8;
  }
}

@media (min-width: 478px) {
  .media_button_container button {
    width: fit-content;
    font-size: var(--rem);
  }
}

@media (min-width: 1280px) {
  .topics_text {
    display: none;
  }

  .topics {
    padding: var(--rem) var(--px);
    gap: var(--half-rem);
    grid-template-columns: 1fr 1fr 1fr;
  }
}

@media (min-width: 1440px) {
  .topics_container h1 {
    padding: 4rem 0 2rem;
    font-size: 4ch;
  }
}
</style>
