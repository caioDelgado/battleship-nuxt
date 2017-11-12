<template>
  <div class="login">
    <div class="logo column is-4 is-offset-4">
      <logo
        size="250px"/>
    </div>
    <nuxt-child/>
  </div>
</template>

<script>
import Logo from '~/components/Logo'

export default {
  layout: 'simple',
  components: {
    Logo
  }
}
</script>

<style lang="sass">
.login
  margin-top: 150px

.logo
  display: inline-block
  position: relative
  overflow: hidden

.logo-animation
  stroke-dasharray: 2755.800048828125
  stroke-dashoffset: 0
  animation: dash 2.5s alternate

@keyframes dash
  0%
    stroke-dashoffset: -2755

  100%
    stroke-dashoffset: 0

</style>
