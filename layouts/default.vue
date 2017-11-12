<template>
  <div>
    <cc-navbar/>
    <div class="columns">
      <nuxt class="nav-margin"/>
    </div>
  </div>
</template>

<script>
import CcNavbar from '~/components/Navbar'

export default {
  components: {
    CcNavbar
  }
}
</script>

<style lang="sass">
.nav-margin
  margin-top: 75px
  padding: 20px
</style>
