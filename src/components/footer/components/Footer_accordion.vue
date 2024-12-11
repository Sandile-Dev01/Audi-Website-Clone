<template>
  <div id="faq">
    <!-- Topics -->
    <li>
      <label htmlFor="1">
        Topics
        <span className="faq_icon">
          <i class="fa-solid fa-chevron-down"></i>
        </span>
      </label>
      <input type="radio" name="pricing" id="1" />
      <div className="content">
        <p>Company</p>
        <p>Models</p>
        <p>Brand</p>
        <p>Career</p>
      </div>
    </li>

    <!-- Audi ag -->
    <li>
      <label htmlFor="2">
        AUDI AG
        <span className="faq_icon">
          <i class="fa-solid fa-chevron-down"></i>
        </span>
      </label>
      <input type="radio" name="pricing" id="2" />
      <div className="content">
        <p>Audi Report 2022</p>
        <p>Documents & Policies</p>
        <p>Financial Calender</p>
        <p>Profile</p>
      </div>
    </li>

    <!-- Services -->
    <li>
      <label htmlFor="3">
        Services
        <span className="faq_icon">
          <i class="fa-solid fa-chevron-down"></i>
        </span>
      </label>
      <input type="radio" name="pricing" id="3" />
      <div className="content">
        <p>myAudi</p>
        <p>Press</p>
        <p>Contact</p>
        <p>Job portal</p>
      </div>
    </li>
  </div>
</template>

<script>
export default {
  name: "Footer_accordion",
};
</script>

<style scoped>
@media (min-width: 0) {
  #faq {
    padding: 0;
    margin: var(--rem) auto;
    width: 100%;
  }

  i {
    color: var(--darker-accent);
  }

  li {
    list-style: none;
  }

  li label {
    font-family: var(--ff-secondary);
    /* background-color: red; */
    border-bottom: 1px solid var(--darker-accent);
    width: 100%;
    cursor: pointer;
    padding: 1.5rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
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
    background-color: var(--darker-accent);
    color: var(--light);
    display: flex;
    align-items: start;
    flex-direction: column;
  }

  p {
    font-size: 13px;
    padding: var(--rem) 0;
    cursor: pointer;
    transition: var(--transition);
  }

  p:hover {
    color: var(--dark-accent);
  }

  label + input[type="radio"]:checked + .content {
    animation: scaleIn 350ms ease-in forwards;
  }
}

@media (min-width: 1025px) {
}

@media (min-width: 600px) {
}

/* Animations */

@keyframes scaleIn {
  0% {
    opacity: 0;
    max-height: 0;
  }
  100% {
    opacity: 1;
    max-height: 500px;
    /* scale: 1; */
  }
}
</style>
