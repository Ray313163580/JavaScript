<template>
  <div>
    <div class="w__loading-bar">
      <div class="w__loading-bar--bar" :class="isError ? 'w__loading-bar--error' : ''" role="bar"
        :style="{transform: 'translate3d(-' + (100 - totalProgress) + '%, 0, 0)'}">
        <div class="w__loading-bar--peg"></div>
      </div>
      <div v-if="showSpinner" class="w__loading-bar--spinner" role="spinner">
        <div class="spinner-icon" :class="isError ? 'spinner-icon--error' : ''"
          :style="{'animation': 'w-spinner 400ms' + easing + ' infinite'}"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'WLoadingBar',
  components: {},
  created () {
  },
  data () {
    return {
      speed: 5,
      easing: 'linear',
      percentNum: 0,
      totalProgress: 0,
      showSpinner: true,
      isError: false
    }
  },
  props: {
    type: {
      type: Number,
      default: 1
    }
  },
  mounted () {
  },
  computed: {},
  methods: {}
}
</script>
<style scoped>
</style>
