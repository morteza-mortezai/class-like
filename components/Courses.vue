<!-- Please remove this file from your project -->
<template>
  <div class="py-12">
    <v-container>
      <v-row>
        <v-col cols="12">
          <h2 class="h2 text-center">معروف ترین دوره ‌هامون</h2>
          <div class="text-subtitle text-center">
            همیشه تو محبوب‌ترین‌ها یه دوره خوب که دنبالشی پیدا میشه
          </div>
        </v-col>
        <v-col cols="6" md="4" v-for="(c, i) in courses" :key="i">
          <course-card :data="c" />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'nuxt-property-decorator'
import { ICourse } from '~/models/course'
import CourseCard from '~/components/CourseCard.vue'
@Component({ components: { CourseCard } })
export default class Courses extends Vue {
  @Prop() readonly data!: ICourse
  courses: ICourse[] = [
    {
      src: 'c1.jpg',
      title: 'طراحی سایت با وردپرس',
      price: 120,
      detail: 'جزئیات',
      count: 2,
    },
    {
      src: 'c2.jpg',
      title: 'طراحی سایت با وردپرس',
      price: 120,
      detail: 'جزئیات',
      count: 2,
    },
    {
      src: 'c3.jpg',
      title: 'طراحی سایت با وردپرس',
      price: 120,
      detail: 'جزئیات',
      count: 2,
    },
  ]
}
</script>
