<template>
  <div>
    <form class="padding-content">
      <div class="field">
        <label class="label">Usuário</label>
        <p class="control">
          <input
            autofocus
            class="input"
            type="text"
            placeholder="Digite seu usuário"
          >
        </p>
      </div>
      <div class="columns">
        <div class="column is-6">
        </div>
      </div>
      <div class="field">
        <p class="control right">
          <button @click.prevent="nextStep" class="button is-primary">Continuar</button>
        </p>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    nextStep () {
      this.$router.push({ path: 'step-two' })
    }
  }
}
</script>
