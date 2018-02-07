<template>
  <div class="col-sm-9 col-md-10 col-xs-8">
    <input id="nomeFile" type="text" class="input form-control" name="nomeFile" data-fv-regexp="true" data-fv-regexp-regexp="^[^*.,;:&%\s]+$" data-fv-regexp-message="Il nome del file non può contenere i seguenti caratteri: ">

    <label class="floating-label">Nome del file</label>       
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      default: ''
    }
  }/*,
  computed: {
    listeners () {
      return {
        // Pass all component listeners directly to input
        ...this.$listeners,
        // Override input listener to work with v-model
        input: event => this.$emit('input', event.target.value)
      }
    }
  }*/
}
</script>

<style lang="scss" scoped>
@import '../variables.scss';

.input {
  width: 100%;
  padding: 8px 10px;
  border: 1px solid $vue-blue;
}
</style>
