<template>
  <div>
    <hero />
    <courses />
  </div>
</template>

<script>
import Courses from '~/components/Courses.vue'
import Hero from '~/components/Hero.vue'
export default {
  name: 'IndexPage',
  components: { Courses, Hero },
}
</script>
