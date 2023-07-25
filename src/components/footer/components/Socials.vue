<template>
  <span>
    <a href="https://www.linkedin.com/in/sandilendimande/" target="_blank"
      ><i class="fa-brands fa-linkedin"></i
    ></a>
    <a href="https://github.com/Sandile-Dev01" target="_blank">
      <i class="fa-brands fa-instagram"></i
    ></a>
    <a href="https://www.sandilendimande.com/" target="_blank"
      ><i class="fa-brands fa-facebook-f"></i
    ></a>
    <a href="https://www.youtube.com/@Sandile-Dev01" target="_blank">
      <i class="fa-brands fa-youtube"></i
    ></a>
  </span>
</template>

<script>
export default {
  name: "Socials",
};
</script>

<style scoped>
@media (min-width: 0) {
  span {
    display: flex;
    align-items: center;
    justify-content: end;
    gap: calc(var(--rem) * 2);
    padding: calc(var(--rem) * 3) calc(var(--rem) * 1.8) var(--rem);
  }

  a {
    font-size: calc(var(--rem) * 1.8);
    cursor: pointer;
    transition: var(--transition);
    color: var(--light);
  }

  a:hover {
    color: var(--dark-accent);
  }
}

@media (min-width: 1025px) {
  span {
    padding: 0;
  }
}
</style>
