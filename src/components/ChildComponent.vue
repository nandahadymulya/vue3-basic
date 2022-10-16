<template>
  <header>
    <slot />
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
