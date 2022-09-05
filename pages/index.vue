<template>
  <section class="home">
    <div class="hooper">
      <img src="./../assets/images/Group 13.svg" alt="" />
      <hooper :settings="hooperSettings">
        <slide>
          <div class="slider1"></div>
        </slide>
        <slide>
          <div class="slider1 slider2"></div>
        </slide>
        <slide>
          <div class="slider1 slider3"></div>
        </slide>
        <hooper-navigation slot="hooper-addons"></hooper-navigation>
        <hooper-pagination slot="hooper-addons"></hooper-pagination>
        <hooper-progress slot="hooper-addons"></hooper-progress>
      </hooper>
    </div>
    <div class="title">{{  $tt(mainProducts.sneakers_product.title_tm,mainProducts.sneakers_product.title_ru) }}</div>
    <div class="cards">
      <Card
        v-for="(e, i) in mainProducts.sneakers_product.sneakers"
        :key="i"
        :info="e"
      />
    </div>
    <!-- <Registration/> -->
  </section>
  </template>

<script>
import Card from "~/components/card/card.vue";
// import Registration from "~/components/registration/registration.vue";

import {
  Hooper,
  Slide,
  Progress as HooperProgress,
  Pagination as HooperPagination,
  Navigation as HooperNavigation,
} from "hooper";
import "hooper/dist/hooper.css";

export default {
  components: {
    Card,
    Hooper,
    // Registration,
    Slide,
    HooperProgress,
    HooperPagination,
    HooperNavigation,
  },

  data() {
    const mainProducts = {
      sneakers_product: {
        title_tm: "TAZE KOLLEKSIYA",
        title_ru: "НОВАЯ КОЛЛЕКЦИЯ",
        sneakers: [
          {
            id: 1,
            img: "12.jpeg",
            text: "sneakers",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
            discount: false,
            added: 0,
          },
          {
            id: 2,
            img: "2.jpeg",
            text: "Nike air jordan 1 low",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
            discount: false,
            added: 0,
          },
          {
            id: 3,
            img: "3.jpeg",
            text: "Nike Sb Dunk",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
            discount: false,
            added: 0,
          },
          {
            id: 4,
            img: "4.jpeg",
            text: "Adidas Yeezy Boost 500",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
            discount: false,
            added: 0,
          },
          {
            id: 5,
            img: "5.jpeg",
            text: "Nike air jordan 1 low",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
            discount: false,
            added: 0,
          },
          {
            id: 6,
            img: "1.svg",
            text: "Nike Sb Dunk",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
            discount: false,
            added: 0,
          },
          {
            id: 7,
            img: "11.jpeg",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
            discount: false,
            added: 0,
          },
          {
            id: 8,
            img: "3.svg",
            text: "Nike air jordan 1 low",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
            discount: false,
            added: 0,
          },
          {
            id: 9,
            img: "9.jpeg",
            text: "Nike Sb Dunk",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
            discount: false,
            added: 0,
          },
          {
            id: 10,
            img: "10.jpeg",
            text: "Nike air jordan 1 low",
            size: "36-44",
            price: "999",
            old_price: "1200",
            href: "",
            new: true,
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

  computed: {
    hooperSettings() {
      const settings = {
        itemsTOShow: 1,
        centerMode: false,
        autoPlay: true,
        playSpeed: 4000,
        transition: 1100,
        hoverPause: false,
        infiniteScroll: true,
        wheelControl: false,
      };
      return settings;
    },
  },
};
</script>

<style></style>
