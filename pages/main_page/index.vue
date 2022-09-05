<template>
  <section class="main_page">
    <div class="man">
      <img src="./../../assets/images/bart.svg" alt="" />
      <p class="one">{{ $tt('Oglanlar üçin','Мужской') }}</p>

      <div class="hidden">
        <nuxt-link to="/">Nike</nuxt-link>
        <nuxt-link to="/">Ecco</nuxt-link>
        <nuxt-link to="/">Asics</nuxt-link>
        <nuxt-link to="/">Adidas</nuxt-link>
        <nuxt-link to="/">New Balance</nuxt-link>
        <nuxt-link to="/">Футбольные</nuxt-link>
        <nuxt-link to="/">Баскетбольные</nuxt-link>
      </div>
    </div>
    <div class="women">
      <img src="./../../assets/images/liza.svg" alt="" />
      <p class="one">{{ $tt('Zenanlar üçin','Женский') }}</p>
      <div class="hidden">
        <nuxt-link to="/">Nike</nuxt-link>
        <nuxt-link to="/">Ecco</nuxt-link>
        <nuxt-link to="/">Asics</nuxt-link>
        <nuxt-link to="/">Adidas</nuxt-link>
        <nuxt-link to="/">New Balance</nuxt-link>
        <nuxt-link to="/">Футбольные</nuxt-link>
        <nuxt-link to="/">Баскетбольные</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style></style>
