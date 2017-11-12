<template>
  <div class="column is-12">
    <div class="columns">
      <div class="column is-6">
        <div class="box">
          <table-board ref="tableBoardUs" :itsMe="false"></table-board>
        </div>
      </div>
      <div class="column is-6">
        <div class="box">
          <table-board ref="tableBoardThem" :itsMe="true"></table-board>
        </div>
      </div>
    </div>
    <nuxt-child/>
  </div>
</template>

<script>
  import TableBoard from '~/components/TableBoard'
  import FleetBoard from '~/components/FleetBoard'
  export default {
    data () {
      return {
        idShip: 0,
        shipsFleet: [
          {id: 1, src: 'ship1.png', length: 1},
          {id: 2, src: 'ship2.png', length: 2},
          {id: 3, src: 'ship3.png', length: 3},
          {id: 4, src: 'ship4.png', length: 4},
          {id: 5, src: 'ship5.png', length: 5}
        ],
        orientation: 'H'
      }
    },
    components: {
      TableBoard,
      FleetBoard
    },
    methods: {
      select (args) {
        this.idShip = args
        this.$refs.tableBoard.setShip(args)
      }
    }
  }
</script>

<style lang="sass" scoped>
  .icon-edit
    font-size: 24px
    color: #ffa726
    cursor: pointer
  .fa-thumbs-o-down
    font-size: 62px
    color: #e34120
  .title
    font-size: 20px
</style>
