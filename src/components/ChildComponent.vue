<script>
export default {
  data() {
    return {
      title: "Title from Child",
      main: "Main from Child",
      section: "Section from Child",
      footer: "Footer from Child",
    };
  },
};
</script>

<template>
  <header>
    <slot :data="title" />
  </header>
  <main>
    <slot name="main" />
  </main>
  <section>
    <slot name="section" />
  </section>
  <footer>
    <slot name="footer" />
  </footer>
</template>
