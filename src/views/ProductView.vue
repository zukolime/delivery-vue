<template>
  <section class="products">
    <div class="container">
      <div class="products-wrapper" id="goods-container">
        <div class="products-card" v-for="goods in goodsArray" :key="goods.id">
          <div class="products-card__image">
            <img :src="getUrl(goods.image)" alt="goods" />
          </div>
          <div class="products-card__description">
            <div class="products-card__description-row">
              <h5 class="products-card__description--name">
                Ролл угорь стандарт
              </h5>
            </div>
            <div class="products-card__description-row">
              <p class="products-card__description--text">
                Рис, угорь, соус унаги, кунжут, водоросли нори.
              </p>
            </div>
            <div class="products-card__description-row">
              <div class="products-card__description-controls">
                <button class="btn btn-primary">
                  В корзину
                  <img
                    src="../assets/img/icons/cart-white.svg"
                    alt="cart-white"
                  />
                </button>
                <span class="products-card__description-controls--price"
                  >250 ₽</span
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { goodsArray } from "../constants/goods";
const getUrl = (name) => {
  return new URL(`../assets/img/goods/${name}`, import.meta.url);
};
</script>
