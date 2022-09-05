<template>
  <nav>
    <div class="top" v-if="!scrolled">
      <div class="contacts">
        <div class="delivery">
          <p>{{ $tt("Eltip bermek", "Доставка") }}</p>
          <img src="./../assets/images/icons/chevron-down.svg" alt="" />
          <div class="menu">
            <ul>
              <li v-for="(e, i) in delivery" :key="i">
                {{ $tt(e.name_tm, e.name_ru) }}
              </li>
            </ul>
          </div>
        </div>
        <div class="contact">
          <img src="./../assets/images/icons/clock.svg" alt="" />
          <p>{{ $tt("9:00dan 18:00-a çenli", "с 9:00 до 18:00") }}</p>
        </div>
        <div class="contact">
          <img src="./../assets/images/icons/phone.svg" alt="" />
          <p>+99362527979</p>
        </div>
        <div class="contact">
          <img src="./../assets/images/icons/instagram.svg" alt="" />
          <p>@sneakers.store.tm</p>
        </div>
        <div class="contact">
          <img src="./../assets/images/icons/Icon-TiktokLogo.svg" alt="" />
          <p>@sneakers.storetm</p>
        </div>
      </div>
    </div>
    <div class="bottom">
      <nuxt-link to="/" class="logo">
        <img src="./../static/Logo.svg" alt="" />
      </nuxt-link>
      <ul>
        <li v-for="(e, i) in nav_links" :key="i">
          <nuxt-link :to="e.href">{{ $tt(e.name_tm, e.name_ru) }}</nuxt-link>
        </li>
        <li @click="showReg"><nuxt-link to="">{{ $tt('Agza Bol','Регистрация') }}</nuxt-link></li>
      </ul>
      <div class="nav_icons">
        <!-- <button @click="showReg">Show</button>
        <button @click="dontShow">Dont Show</button> -->
        <img src="./../assets/images/icons/Search.svg" alt="" />
        <img src="./../assets/images/icons/Shopping-card.svg" alt="" />
        <div class="lang_btn" v-for="(e, i) in locales" :key="i">
          <nuxt-link to="">
            <button @click="$i18n.setLocale(e.code)">
              {{ e.name }}
            </button>
          </nuxt-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      scrolled: false,
      delivery: [
        {
          name_tm: "Ashgabat",
          name_ru: "Ашхабат",
        },
        {
          name_tm: "Balkan",
          name_ru: "Балкан",
        },
        {
          name_tm: "Lebap",
          name_ru: "Лебап",
        },
        {
          name_tm: "Mary",
          name_ru: "Мары",
        },
        {
          name_tm: "Ahal",
          name_ru: "Ахал",
        },
        {
          name_tm: "Daşoguz",
          name_ru: "Дашогуз",
        },
      ],
      nav_links: [
        {
          href: "/main_page",
          name_tm: "Baş sahypa",
          name_ru: "Главное",
        },
        {
          href: "/availability",
          name_tm: "Elimizdaki",
          name_ru: "Наличие",
        },
        {
          href: "/order",
          name_tm: "Zakaz",
          name_ru: "Заказ",
        },
        {
          href: "/discounts",
          name_tm: "Arzanladyş",
          name_ru: "Скидки",
        },
        // {
        //   href: "/",
        //   name_tm: "Agza Bol",
        //   name_ru: "Регистрация",
        // },
      ],
    };
  },
  beforeMount() {
    // let nav_bar = document.querySelector('.header');
    window.onscroll = () => {
      if (scrollY > 80) {
        this.scrolled = true;
        // nav_bar.classList.add('scrolled_nav')
      } else {
        this.scrolled = false;
        // nav_bar.classList.remove('scrolled_nav')
      }
    };
  },
  computed: {
    lang() {
      return this.$i18n.locale;
    },
    locales() {
      return this.$i18n.locales;
    },
  },
  methods: {
    showReg() {
      this.$store.dispatch("showReg");
    },
    dontShow() {
      this.$store.dispatch("dontShow");
    },
  },
};
</script>
<style></style>
