<template>
    <section class="order">
    <div class="title_card">{{ $tt(mainProducts.sneakers_product.title_tm,mainProducts.sneakers_product.title_ru) }}</div>
    <div class="cards">
      <Card
        v-for="(e, i) in mainProducts.sneakers_product.sneakers"
        :key="i"
        :info="e"
      />
    </div>
  </section>
</template>

<script>
  import Card from '@/components/card/card.vue'
export default {
components:{
    Card
},
data() {
    const mainProducts = {
      sneakers_product: {
        title_tm: 'ZAKAZ EDIŇ',
        title_ru: 'НА ЗАКАЗ',
        sneakers: [
          {
            id: 1,
            img: "25.svg",
            text: "Nike air jordan 1 low",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,
          },
          {
            id: 2,
            img: "4.jpeg",
            text: "Nike air jordan 1 low",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,

          },
          {
            id: 3,
            img: "23.svg",
            text: "Nike Sb Dunk",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,
          },
          {
            id: 4,
            img: "22.svg",
            text: "Nike air jordan 1 low",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,
          },
          {
            id: 5,
            img: "21.svg",
            text: "Nike Sb Dunk",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,

          },
          {
            id: 6,
            img: "20.svg",
            text: "Nike air jordan 1 low",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,
          },
          {
            id: 7,
            img: "19.svg",
            text: "Adidas Yeezy Boost 500",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,

          },
          {
            id: 8,
            img: "18.svg",
            text: "Nike Sb Dunk",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,
          },
          {
            id: 9,
            img: "17.svg",
            text: "Nike air jordan 1 low",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,
          },
          {
            id: 10,
            img: "16.svg",
            text: "Nike Sb Dunk",
            size: "36-44",
            price: "999",
            old_price: "1250",
            href: "",
            new: false,
            discount: false,
            added: 0,

          },
        ],
      },
    };
    return {
      mainProducts,
    };
  },
}
</script>

<style>

</style>