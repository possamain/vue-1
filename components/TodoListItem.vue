<template>
  <option value="json">{{ todo.text }}
</option>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true
    }
  }
}
</script>