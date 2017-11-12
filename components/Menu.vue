<template>
  <div class="column is-2 aside">
    <aside class="menu animated slideInLeft">
      <ul class="menu-list">
        <li v-for="item in items"><nuxt-link :to="item.path">
          <span class="icon is-small space">
            <i class="fa" :class="item.fa"></i>
          </span>
          {{ item.name }}
        </nuxt-link></li>
        <li><a href="#">
          <span class="icon is-small space">
            <i class="fa fa-sign-out"></i>
          </span>
          Sair
        </a></li>
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      default () {
        return [{
          name: 'Item',
          path: '/',
          fa: 'fa-diamond'
        }]
      }
    }
  }
}
</script>

<style lang="sass" scoped>
.menu
  background: linear-gradient(to right, #2193b0 0%, #26a0da 100%)
  height: 100%
  z-index: 1
  padding-top: 65px
.menu-list a
  color: white
  opacity: 100
  font-size: 15px
  padding: 5px 14px
.menu-list a:hover
  background-color: #b9d1da
  color: #2193b0
.menu-list a.is-active
  background-color: #b9d1da
  color: #2193b0
.icon.is-small
  line-height: 26px
@media (min-width: 700px)
  .menu
    position: fixed
    width: 15.1%
    padding-top: 65px
@media print
  .menu
    display: none
</style>
