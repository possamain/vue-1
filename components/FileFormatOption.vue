<template>
  <option v-if="format" value="json">{{ format.text }}</option>
</template>

<script>
export default {
  props: {
    format: {
      type: Object,
      required: true
    }
  }
}
</script>