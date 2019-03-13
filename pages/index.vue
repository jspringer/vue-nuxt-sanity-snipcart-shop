<template>
  <section>
    <div>
      <h1 class="title">
        <a href="https://jsnspr-vue-nuxt-sanity-snipcart-shop.netlify.com">
          <AppLogo />
        </a>
      </h1>
      <h2 class="subtitle">
        International chocolate and candy.
      </h2>
    </div>
  </section>
</template>

<script>
import AppLogo from "~/components/AppLogo"

export default {
  components: {
    AppLogo
  }
}
</script>

<style scoped>
section {
  background-size: cover;
}

.title,
.subtitle {
  text-align: center;
  padding: 1em;
}

.title {
  font-size: 10vw;
  padding-bottom: 0.5em;
}

.subtitle {
  padding-bottom: 3em;
}
</style>
