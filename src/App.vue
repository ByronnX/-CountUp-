<template>
  <vue-count-up :end="2500" :duration="2.5"></vue-count-up>
</template>

<script>
import { CountUp } from 'countup.js'
import VueCountUp from './VueCountUp.vue';
export default {
  name: 'countup-remake',
  components: {
    VueCountUp
  },
  data() {

  },
  mounted() {
  },
  methods: {

  },
  props: {

  }
}
</script>
