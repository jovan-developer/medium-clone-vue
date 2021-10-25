<template>
  <div>
    <mcv-top-bar />
    <router-view />
  </div>
</template>

<script>
import McvTopBar from '@/components/TopBar'
import {actionTypes} from '@/store/modules/auth'

export default {
  name: 'McvApp',
  components: {
    McvTopBar
  },
  mounted() {
    console.log('Hello App')
    this.$store.dispatch(actionTypes.getCurrentUser)
  }
}
</script>
