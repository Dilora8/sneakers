<template>
  <div class="inputs">
    <div class="exit">
      <svg
        @click="dontShow"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M18 6L6 18"
          stroke="black"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
        <path
          d="M6 6L18 18"
          stroke="black"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </div>
    <div class="content">
      <p>Agza bol</p>
      <div class="forms">
        <div class="form" v-for="(e, i) in inputs" :key="i">
          <label>{{ e.label }}</label>
          <input :type="e.type" v-model="models[i]" />
        </div>
      </div>
      <div class="btn">
        <nuxt-link to=""><button class="btn1" @click="submit">Agza bol</button></nuxt-link>
       <nuxt-link to=""><p>Hasaba alynan</p></nuxt-link>
        <nuxt-link to=""><button class="btn2">Hasaba gir</button></nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    const inputs = [
      {
        id: 1,
        label: "Ady",
        type: "text",
      },
      {
        id: 2,
        label: "Nomer",
        type: "number",
      },
      {
        id: 3,
        label: "Parol",
        type: "password",
      },
      {
        id: 4,
        label: "Tazeden parol",
        type: "Password",
      },
      {
        id: 5,
        label: "Salgynyz",
        type: "text",
      },
    ]

    const datas = {
      name: '',
      phone: null,
      password: '',
      password: '',
      adress: '',
    }
    const input_values = []
    return {
      models:[
      datas.name,
      datas.phone,
      datas.password,
      datas.password,
      datas.adress,
      ],
      inputs,
      datas,
      input_values,
    };
  },
  methods: {
    showReg() {
      this.$store.dispatch("showReg");
    },
    dontShow() {
      this.$store.dispatch("dontShow");
    },
    submit() {
      this.datas.name =this.models[0]
      this.datas.phone =this.models[1]
      this.datas.password =this.models[2]
      this.datas.password =this.models[3]
      this.datas.adress =this.models[4]
    }
  },
};
</script>

<style>
</style>