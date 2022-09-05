<template>
 
    <nuxt-link :to="'/product/'+info.id" class="card">
    <div class="img">
      <img :src="require(`~/assets/images/product/${info.img}`)" alt="" />
    </div>
    <div class="text">
      <p>{{ info.text }}</p>
    </div>
    
    <div class="bottom">
      <div>
        <div class="old_price">
          <p>{{ info.old_price }}TDM</p>
        </div>
        <div class="price">
          <p>{{ info.price }}TDM</p>
        </div>
      </div>
      <div>
        <div class="size">
          <p>Size: {{ info.size }}</p>
        </div>
        <div class="add_sebet" v-if="info.added === 0 && !show" @click.prevent="add">
          <button>{{ $tt('Sebede goş','Добавить') }}</button>
          <svg
            class="btns"
            width="40"
            height="40"
            viewBox="0 0 40 40"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <circle cx="20" cy="20" r="20" fill="#E90909" />
            <rect
              width="18.2857"
              height="18.2857"
              transform="translate(10.8572 10.8571)"
              fill="#E90909"
            />
            <path
              d="M24 24H15.8429L13.85 13.0428C13.8267 12.9116 13.7582 12.7927 13.6565 12.7066C13.5548 12.6205 13.4261 12.5727 13.2929 12.5714H12"
              stroke="white"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M16.5714 26.8571C17.3604 26.8571 18 26.2175 18 25.4286C18 24.6396 17.3604 24 16.5714 24C15.7824 24 15.1428 24.6396 15.1428 25.4286C15.1428 26.2175 15.7824 26.8571 16.5714 26.8571Z"
              stroke="white"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M24.0001 26.8571C24.7891 26.8571 25.4287 26.2175 25.4287 25.4286C25.4287 24.6396 24.7891 24 24.0001 24C23.2111 24 22.5715 24.6396 22.5715 25.4286C22.5715 26.2175 23.2111 26.8571 24.0001 26.8571Z"
              stroke="white"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M15.3214 21.1428H24.2928C24.5599 21.1436 24.8188 21.0503 25.0239 20.8791C25.229 20.708 25.3672 20.47 25.4142 20.2071L26.2856 15.4285H14.2856"
              stroke="white"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </div>
        <div class="added_sebet" v-else>
          <button @click="remove">-</button>
          <p>{{ info.added }}</p>
          <button @click="add">+</button>
        </div>
      </div>
    </div>
    <div class="new" v-if="info.new"><P>Täze</P></div>
    <div class="percent" v-if="info.discount">
      <p>%</p>
    </div>
  </nuxt-link>

  
</template>

<script>
export default {
  props: {
    info: {
      type: Object,
      required: true,
    },

  },
  data(){
    return{
      show: false
    }
  },
  methods: {
    add() {
      this.show = !this.show
      this.info.added += 1;
    },
    remove() {
      this.info.added -= 1;
    },
  },
};
</script>

<style></style>
