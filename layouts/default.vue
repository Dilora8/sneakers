<template>
  <div class="main">
    <div class="header">
      <Header />
    </div>
    <nuxt />
    <Registration v-if="showRegState"/>
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/header.vue";
import Registration from "@/components/registration/registration.vue";
import Footer from "@/components/footer/footer.vue";
export default {
  name: "DefaultLayout",
  components: {
    Header,
    Registration,
    Footer,
  },
  data() {
    return {
      
    };
  },
  computed:{
    showRegState(){
      return this.$store.getters.showReg;
    }
  }
};
</script>
