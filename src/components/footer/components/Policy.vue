<template>
  <div class="policies_container">
    <div class="copyright_text_container">
      <span class="copyright">
        &#x00A9; AUDI AG. Developed by
        <a href="https://www.linkedin.com/in/sandilendimande/" target="_blank"
          >Sandile Ndimande</a
        >
      </span>

      <span class="links">
        <p>Legal Notice</p>
        <p>Legal</p>
        <p>Whistleblower System</p>
        <p>Privacy Policy</p>
        <p>Cookie Policy</p>
        <p>Cookie Consent Options</p></span
      >
    </div>

    <span class="lang_accordion">
      <i class="fa-solid fa-globe"></i>
      <select name="" id="">
        <option value="English">
          English &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        </option>
        <option value="Deutsch">
          Deutsch &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        </option>
      </select>
    </span>
  </div>
</template>

<script>
export default {
  name: "Policy",
};
</script>

<style scoped>
@media (min-width: 0) {
  .policies_container {
    padding: calc(var(--rem) * 4) calc(var(--rem) * 1.8) calc(var(--rem) * 2);

    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 0.75rem;
    flex-wrap: wrap;
  }

  .policies_container .links {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    cursor: pointer;
    transition: var(--transition);
  }

  p {
    transition: var(--transition);
    font-weight: var(--bolder);
    color: var(--light-accent);
  }

  p:hover {
    color: var(--dark-accent);
    transform: translateY(-1px);
  }

  .copyright_text_container {
    display: flex;
    gap: var(--rem);
    flex-wrap: wrap;
  }

  .copyright {
    margin-right: auto;
  }

  .copyright a {
    color: var(--dark-accent);
    cursor: pointer;
    transition: var(--transition);
    font-size: 0.85rem;
    position: relative;
    transform: translate(-50%, -50%);
  }

  .copyright a::after {
    content: "";
    position: absolute;
    top: -50%;
    left: -50%;

    padding: 0.5rem;
  }

  .copyright a:hover {
    color: rgb(221, 221, 220);
    text-decoration: none;
  }

  .copyright a:hover::after {
    backdrop-filter: blur(1px);
    border-top: 1px solid var(--light-accent);
    border-bottom: 1px solid var(--light-accent);

    height: 100%;
    animation: animateIt 3s ease-in-out alternate infinite;
  }

  .copyright a:active::after {
    backdrop-filter: invert(2);

    height: 100%;
    animation: animateIt 3s ease-in-out alternate infinite;
  }

  .lang_accordion {
    display: flex;
    align-items: center;
    gap: 5px;
  }

  .lang_accordion i {
    font-size: 1.5rem;
  }

  select,
  select.lang_accordion {
    cursor: pointer;
    font-family: var(--ff-primary);
    background-color: var(--dark);
    color: var(--light);
    outline: none;
    border: none;
    margin: 1rem 0;
  }
}

@media (min-width: 600px) {
  .policies_container .links {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    gap: 0.5rem;
    cursor: pointer;
    transition: var(--transition);
  }
}

@media (min-width: 980px) {
  .policies_container {
    flex-wrap: nowrap;
  }
}

@media (min-width: 1025px) {
  .policies_container {
    padding: 0;
    margin-bottom: calc(var(--rem) * 4);
  }
}

@media (min-width: 1088px) {
  .copyright {
    margin: 0;
  }
}

@keyframes animateIt {
  0% {
    width: 10%;
    left: 0;
    scale: 1;
  }
  25% {
    scale: 1;
  }
  50% {
    scale: 1;
    width: 25%;
  }
  100% {
    width: 5%;
    left: 95%;
    scale: 0;
    border-radius: 1rem;
  }
}
</style>
