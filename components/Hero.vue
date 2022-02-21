<style lang="scss" scoped>
.bg {
  background-color: rgb(243, 244, 246);
}
.hero {
  display: flex;
  &-detail {
    margin: 80px 0 0 0;
    flex-grow: 1;
  }
  &-img {
    flex-basis: 30%;
  }
}
</style>
<template>
  <div class="bg">
    <v-container>
      <div class="hero">
        <div class="hero-detail">
          <h1 class="h1">کمترین فاصله با جهان</h1>
          <p class="mt-2">یادگیری آنلاین با موثرترین روش</p>
          <v-text-field
            class="mt-12"
            full-width
            outlined
            prepend-inner-icon="mdi-magnify"
            rounded
            solo
            flat
            filled
            placeholder="دوره مورد نظرت رو جستجو کن ..."
          />
        </div>
        <div class="hero-img">
          <img src="~/static/Home-Vector-rtl.svg" alt="" />
        </div>
      </div>
    </v-container>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component
export default class Hero extends Vue {}
</script>
