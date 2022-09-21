<template>
  <div class="wrapper">
    <div class="wrapper-content wrapper-content--fixed">
      <section>
        <div class="container">
          <div class="item__wrapper">
            <shopItem
              v-for="product in shopList"
              :key="product.id"
              :product="product"
            />
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import shopItem from "@/components/ShopItem.vue";
export default {
  components: {
    shopItem,
  },

  data() {
    return {
      shopList: null,
    };
  },
  created() {
    this.shopList = this.$store.getters.getShopList;
  },
};
</script>
