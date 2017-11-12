<template>
  <nav class="nav has-shadow animated slideInDown">
      <div class="column is-12">
        <a class="nav-item">
          <h2>Battleship</h2>
        </a>
      </div>
  </nav>
</template>

<script>
export default {
}
</script>

<style lang="sass" scoped>
@media print
  nav
    display: none
fa
  font-size: 21px
.nav-item a:not(.button).is-tab:hover, a.nav-item:not(.button).is-tab:hover
  border-bottom-color: #00344d
a.nav-item:not(.button)
  color: #00344d
  margin-top: 7px
.nav
  width: 100%
  height: 60px
  position: fixed
@media (min-width: 700px)
  .menu
    position: fixed
    width: 14.1%
.bars
  margin-top: 16px
  cursor: pointer
  float: left
</style>
