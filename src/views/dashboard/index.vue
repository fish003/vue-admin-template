<template>
  <div class="dashboard-container">
    <div class="dashboard-text">name: {{ name }}</div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Dashboard',
  computed: {
    ...mapGetters([
      'name'
    ])
  },
  mounted() {
    console.log(process.env.VUE_APP_BASE_API,'appindex');
    console.log(process,'appindex1');
    console.log(process.env,'appindexenv');
    console.log(process.env.VUE_APP_TEST_KEY_ONE,'appindexone');
    console.log(process.env.VUE_APP_TEST_KEY_TWO,'appindextwo');
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
