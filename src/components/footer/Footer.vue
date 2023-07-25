<template>
  <footer>
    <Socials />

    <div class="footer_links_container">
      <!-- Topics footer links -->

      <Footer_links
        header="Topics"
        link_item_1="Company"
        link_item_2="Models"
        link_item_3="Brand"
        link_item_4="Career"
      />

      <!-- Audi Ag -->

      <Footer_links
        header="AUDI AG"
        link_item_1="Audi Report 2022"
        link_item_2="Documents & Policies"
        link_item_3="Financial Calender"
        link_item_4="Profile"
      />

      <!-- Services -->

      <Footer_links
        header="Services"
        link_item_1="myAudi"
        link_item_2="Press"
        link_item_3="Contact"
        link_item_4="Job portal"
      />
    </div>

    <div class="footer_accordion">
      <Footer_accordion />
    </div>

    <!-- Policies section -->
    <Policy />

    <!-- Footer text section -->
    <Footer_text />
  </footer>
</template>

<script>
import Socials from "./components/Socials.vue";
import Footer_accordion from "./components/Footer_accordion.vue";
import Footer_links from "./components/Footer_links.vue";
import Policy from "./components/Policy.vue";
import Footer_text from "./components/Footer_text.vue";

export default {
  name: "Footer",
  components: {
    Socials,
    Footer_accordion,
    Footer_links,
    Policy,
    Footer_text,
  },
};
</script>

<style scoped>
@media (min-width: 0) {
  footer {
    color: var(--light);
    background-color: var(--dark);
  }

  .footer_links_container {
    display: none;
  }
}

@media (min-width: 600px) {
  .footer_accordion {
    display: none;
  }

  .footer_links_container {
    /* padding: calc(var(--rem) * 2) 0 calc(var(--rem) * 5); */
    padding: var(--rem) calc(var(--rem) * 1.8);
    display: flex;
    gap: 15%;
    justify-content: flex-start;
    border-bottom: 1px solid var(--dark-accent);
  }
}

@media (min-width: 1025px) {
  footer {
    padding: calc(var(--rem) * 3) var(--px);
  }

  .footer_links_container {
    padding: calc(var(--rem) * 2) 0;
  }
}
</style>
