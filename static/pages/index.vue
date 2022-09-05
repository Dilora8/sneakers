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
    <div class="title">{{ mainProducts.sneakers_product.title }}</div>
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
import Card from "~/components/card/card.vue";

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
    Slide,
    HooperProgress,
    HooperPagination,
    HooperNavigation,
  },

  data() {
    const mainProducts = {
      sneakers_product: {
        title: 'Täze kolleksiya',
        sneakers: [
          {
            id: 1,
            img: "1.png",
            text: "ztfgjnfgn",
            size: "36-44",
            price: "999",
            href: "",
            new: true,
            precent: false,
            added: 1,
          },
          {
            id: 2,
            img: "1.png",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            href: "",
            new: false,
            precent: false,
          },
          {
            id: 3,
            img: "1.png",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            href: "",
            new: false,
            precent: false,
          },
          {
            id: 4,
            img: "1.png",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            href: "",
            new: false,
            precent: false,
          },
          {
            id: 5,
            img: "1.png",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            href: "",
            new: false,
            precent: false,
          },
          {
            id: 6,
            img: "1.png",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            href: "",
            new: false,
            precent: false,
          },
          {
            id: 7,
            img: "1.png",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            href: "",
            new: false,
            precent: false,
          },
          {
            id: 8,
            img: "1.png",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            href: "",
            new: false,
            precent: false,
          },
          {
            id: 9,
            img: "1.png",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            href: "",
            new: false,
            precent: false,
          },
          {
            id: 10,
            img: "1.png",
            text: "zsrtfgjnyhjmn",
            size: "36-44",
            price: "999",
            href: "",
            new: false,
            precent: false,
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
        playSpeed: 5000,
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
