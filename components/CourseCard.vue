<style scoped lang="scss">
.ccard {
  padding: 11px;
  border-radius: 18px;
  box-shadow: 0 3px 5px 0 rgba($color: #666565, $alpha: 0.15);
  height: 100%;
  &-imgframe {
    width: 100%;
    padding-bottom: 56.25%;

    overflow: hidden;
    position: relative;
    img {
      border-radius: 14px;
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    &-price {
      position: absolute;
      background-color: rebeccapurple;
      color: white;
      bottom: 10px;
      left: 10px;
      border-radius: 20px;
      padding: 4px 8px;
      font-size: 14px;
    }
  }
  &-detail {
    &-title {
    }
    &-footer {
      display: flex;
      padding: 3px 5px;
    }
  }
}
</style>
<template>
  <div class="ccard">
    <div class="ccard-imgframe">
      <img :src="require(`~/static/${data.src}`)" />
      <span class="ccard-img-price">
        {{ data.price }}
      </span>
    </div>
    <div class="detail">
      <h3 class="ccard-detail-title">
        {{ data.title }}
      </h3>
      <p class="ccard-detail-detail">
        {{ data.detail }}
      </p>
      <v-divider></v-divider>
      <div class="ccard-detail-footer">
        <v-icon>mdi-book-open-page-variant-outline</v-icon>
        <v-spacer></v-spacer>
        <v-icon>mdi-share-variant-outline</v-icon>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'nuxt-property-decorator'
import { ICourse } from '~/models/course'

@Component
export default class CourseCard extends Vue {
  @Prop() readonly data!: ICourse
}
</script>
