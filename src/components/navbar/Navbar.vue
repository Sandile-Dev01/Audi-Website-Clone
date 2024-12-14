<template>
  <nav>
    <div class="menu">
      <div
        class="burger_menu"
        @click="(showMenu = !showMenu), (showSearchInput = false)"
      >
        <i
          class="fa-thin fa-dash"
          :class="{ rotate_1: showMenu, 'fa-thin rotate_1_reverse': !showMenu }"
        ></i>
        <i
          class="fa-thin fa-dash"
          :class="{ shrink: showMenu, 'fa-thin shrink_back': !showMenu }"
        ></i>
        <i
          class="fa-thin fa-dash"
          :class="{ rotate_2: showMenu, 'fa-thin rotate_2_reverse': !showMenu }"
        ></i>
      </div>

      <p @click="(showMenu = !showMenu), (showSearchInput = false)">Menu</p>

      <span
        class="menu_mobile_links"
        :class="{ mobileShow: showMenu, mobileHide: !showMenu }"
      >
        <li>Company <i class="fa-solid fa-chevron-down"></i></li>
        <li>Innovation <i class="fa-solid fa-chevron-down"></i></li>
        <li>Models</li>
        <li>Brand</li>
        <li>Careers <i class="fa-solid fa-chevron-down"></i></li>

        <div class="mobile_flag">
          <div class="mobile_flag_nav">
            <img
              src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Flag_of_South_Africa.svg/2560px-Flag_of_South_Africa.svg.png"
              alt="a picture of a South African flag"
            />
          </div>
          <span class="mobile_flag_text">
            <p>Audi in your region:</p>
            <p>South Africa</p>
          </span>
        </div>
      </span>
    </div>

    <div class="logo_links_container">
      <span class="logo">
        <img
          src="https://logos-world.net/wp-content/uploads/2021/03/Audi-Logo.png"
          alt="logo"
        />
      </span>
      <div class="nav_links">
        <li>Company</li>
        <li>Innovation</li>
        <li>Models</li>
        <li>Brand</li>
        <li>Careers</li>
      </div>
    </div>

    <div class="nav_search">
      <span class="search_side">
        <!-- mobile phones and tablets search bar  -->
        <span
          class="search_side min-screens"
          @click="(showSearchInput = !showSearchInput), (showMenu = false)"
        >
          <template v-if="showSearchInput">
            <i class="fa-solid fa-x"></i>
          </template>

          <template v-else>
            <i class="fa-sharp fa-solid fa-magnifying-glass"></i>
          </template>
        </span>

        <!-- pc screens search -->
        <span
          class="search_side"
          :class="{ big_screens: searchClose, big_search_hide: !searchClose }"
        >
          <input type="text" placeholder="Enter search term " />
          <i class="fa-sharp fa-solid fa-magnifying-glass"></i>
          <p v-if="searchClose" @click="searchClose = !searchClose">Close</p>
          <p v-else @click="searchClose = !searchClose">Search</p>
        </span>
      </span>
      <div class="flag">
        <div class="nav_flag">
          <img
            src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Flag_of_South_Africa.svg/2560px-Flag_of_South_Africa.svg.png"
            alt="a picture of a South African flag"
          />
        </div>
        <span class="nav_flag_text">
          <p>Audi in your region:</p>
          <p>South Africa</p>
        </span>
      </div>
    </div>
    <div
      class="nav_search_input"
      :class="{
        nav_search_input: showSearchInput,
        hide_input: !showSearchInput,
      }"
    >
      <input type="search" placeholder="Enter search term" />
      <i class="fa-sharp fa-solid fa-magnifying-glass"></i>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      showMenu: false,
      showSearchInput: false,
      searchClose: false,
    };
  },
};
</script>

<style scoped>
@media (min-width: 0) {
  nav {
    display: flex;
    align-items: center;
    background-color: var(--light);
    justify-content: space-between;
    padding: var(--padding-min);
    position: sticky;
    top: 0;
    z-index: 100;
  }

  .logo_links_container {
    display: flex;
    gap: var(--rem);
  }

  .logo {
    width: 4.5rem;
    object-fit: cover;
    margin-right: calc(var(--rem) * 2);
  }

  .logo img {
    width: 100%;
    cursor: pointer;
    transition: var(--transition);
  }

  .logo img:hover {
    opacity: 0.65;
  }
  .nav_links {
    display: none;
  }

  /* Flag section */

  .nav_search,
  .search_side,
  .menu {
    display: flex;
    align-items: center;
  }

  .search_side.big_screens,
  .search_side.big_search_hide {
    display: none;
  }

  .menu {
    gap: var(--half-rem);
    cursor: pointer;
    position: relative;
  }

  .menu_mobile_links {
    position: absolute;
    top: 225%;
    left: -37%;
    width: 100dvw;
    display: block;

    background-color: rgb(249, 246, 246);
    display: flex;
    flex-direction: column;
    padding: 1rem calc(var(--rem) * 1.8);
    padding-right: auto;

    gap: var(--rem);
  }

  .menu_mobile_links.mobileShow {
    animation: mobileMenuShow 500ms ease-in-out forwards;
  }

  .menu_mobile_links.mobileHide {
    animation: mobileMenuHide 500ms ease-in-out forwards;
  }

  .menu_mobile_links li {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.75rem 0;
    list-style-type: none;
    border-bottom: 1.5px solid var(--light-accent);
  }

  .menu_mobile_links li i {
    font-size: 0.75rem;
    color: var(--dark-accent);
  }

  /* Burger menu */

  .burger_menu {
    width: 1.5rem;
    height: 1rem;
    gap: 10%;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
  }

  .fa-thin {
    display: inline;
    background-color: var(--dark);
    padding: 0.1px;
    width: 100%;
  }

  .fa-thin.shrink_back {
    animation: shrink_back 400ms ease-in forwards;
  }

  .fa-thin.rotate_1_reverse {
    animation: rotate_1_reverse 400ms ease-in forwards;
  }

  .fa-thin.rotate_2_reverse {
    animation: rotate_2_reverse 400ms ease-in forwards;
  }

  .shrink {
    animation: shrink 450ms ease-in forwards;
  }

  .rotate_1 {
    animation: rotate_1 450ms ease-in forwards;
  }

  .rotate_2 {
    animation: rotate_2 450ms ease-in forwards;
  }

  /* Search side */

  .search_side.min-screens {
    width: 1.2rem;
  }

  .search_side {
    cursor: pointer;
    position: relative;
  }

  .search_side p {
    display: none;
  }

  .nav_search_input {
    background-color: var(--light);
    box-shadow: 0 -1px 1rem 1px var(--dark-accent);
    padding: 1rem calc(var(--rem) * 1.8);
    position: absolute;
    z-index: 1;
    right: 0;
    bottom: -3.4rem;
    width: 100%;

    display: flex;
    align-items: center;

    animation: search_move_1 450ms ease-in forwards;
  }

  .nav_search_input input {
    font-family: var(--ff-primary);
    font-size: 1.1rem;
    width: 100%;
    margin-right: calc(var(--rem) * 2);
    padding: auto 0;
    outline: none;
    border: none;
    border-bottom: 2px solid var(--dark);
  }

  .nav_search_input i {
    cursor: pointer;
  }

  .hide_input {
    animation: hide_input 450ms ease-out forwards;
  }

  /* flag section */

  .flag {
    display: none;
  }
  .mobile_flag {
    display: flex;
    align-items: center;
    padding: var(--half-rem) 0;
  }
  .nav_flag,
  .mobile_flag_nav {
    border-radius: 100%;
    width: 2rem;
    height: 2rem;
    object-fit: cover;
    margin-right: var(--half-rem);
    cursor: pointer;
  }

  .nav_flag img,
  .mobile_flag img {
    height: 100%;
    width: 100%;
    border-radius: 100px;
  }

  .mobile_flag_text {
    font-size: 12px;
  }

  .mobile_flag_text :nth-child(1) {
    color: var(--dark-accent);
    font-weight: 900;
  }
}

@media (min-width: 1025px) {
  nav {
    padding: 0 calc(var(--rem) * 1.8);
    border-bottom: 1px solid var(--dark-accent);
  }

  .menu_mobile_links {
    display: none;
  }
  .flag {
    display: flex;
    align-items: center;
    margin: var(--rem);
    padding: 0 var(--half-rem);
  }

  .flag::before {
    content: "";
    height: 1.5rem;
    margin-right: 1rem;
    border: 0.1px solid var(--dark);
  }

  .nav_flag_text {
    display: none;
  }
}

@media (min-width: 1439px) {
  nav {
    padding: 0 var(--px);
  }
  .menu {
    display: none;
  }

  .search_side.min-screens {
    display: none;
  }

  .search_side.big_screens,
  .search_side.big_search_hide {
    display: flex;
  }

  .search_side.big_screens input {
    position: absolute;
    font-family: var(--f-primary);
    font-size: 1.2rem;
    border: none;
    padding: var(--rem) 0;
    border-bottom: 2px solid var(--dark);
    animation: bigSearchInput 350ms ease-in-out forwards;
  }

  .search_side.big_search_hide input {
    position: absolute;
    font-family: var(--f-primary);
    font-size: 1.2rem;
    border: none;
    padding: var(--rem) 0;
    border-bottom: 2px solid var(--dark);
    animation: bigSearchHide 350ms ease-in-out forwards;
    animation-delay: 0s;
  }

  .search_side.big_screens input:focus {
    outline: none;
  }

  .nav_flag_text,
  .search_side p {
    display: inline-block;
    cursor: pointer;
  }

  .nav_flag_text :nth-child(1) {
    color: var(--dark-accent);
    font-weight: 900;
  }

  .search_side {
    gap: var(--rem);
  }

  .nav_search_input {
    display: none;
  }

  .nav_links {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 2rem;
    list-style-type: none;
  }

  .nav_links li {
    cursor: pointer;
    transition: var(--transition);
    display: flex;
    flex-direction: column;
  }

  .nav_links li:hover {
    font-weight: 900;
  }

  .nav_links li::after {
    content: "";
    border-bottom: 2.1px solid var(--dark);
    position: relative;
    bottom: -1.55rem;
    width: 0;
  }

  .nav_links li:hover::after {
    font-weight: 800;
    animation: link_animation 450ms ease-in-out forwards;
  }
}

/* Animations */

@keyframes link_animation {
  0% {
    width: 0;
  }
  100% {
    width: 100%;
  }
}

/* Burger animations */
@keyframes shrink {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    width: 0;
  }
}

@keyframes shrink_back {
  0% {
    opacity: 0;
    width: 0;
  }
  90% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
    width: 100%;
  }
}

@keyframes rotate_1 {
  0% {
    display: inline;
  }
  100% {
    translate: 5px 0.5rem;
    rotate: 45deg;
  }
}

@keyframes rotate_1_reverse {
  0% {
    translate: 5px 0.5rem;
    rotate: 45deg;
  }
  100% {
    translate: 0;
    rotate: 0;
  }
}

@keyframes rotate_2 {
  0% {
    display: inline;
  }
  100% {
    translate: 5px -0.5rem;
    rotate: -45deg;
  }
}

@keyframes rotate_2_reverse {
  0% {
    translate: 5px -0.5rem;
    rotate: -45deg;
  }
  100% {
    translate: 0;
    rotate: 0;
  }
}

@keyframes search_move_1 {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes hide_input {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    display: none;
  }
}

@keyframes bigSearchInput {
  0% {
    opacity: 1;
    translate: 0;
    width: 0;
  }
  100% {
    translate: -56dvw 0;
    width: 56dvw;
    padding-left: 0;
    padding-right: 0rem;
  }
}

@keyframes bigSearchHide {
  0% {
    translate: -56dvw 0;
    width: 56dvw;
    padding-left: 0;
    padding-right: 0rem;
  }
  100% {
    translate: 0;
    width: 0;
  }
}

@keyframes mobileMenuShow {
  0% {
    height: 0;
    opacity: 0;
  }
  100% {
    height: 100vh;
  }
}

@keyframes mobileMenuHide {
  0% {
    height: 100vh;
  }
  100% {
    height: 0;
    opacity: 0;
    display: none;
  }
}
</style>
