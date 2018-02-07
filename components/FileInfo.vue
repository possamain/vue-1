<template>
  <div id="infoFile" class="form-group form-material floating row">
		<FileName
			v-model="newTodoText"
			placeholder="New todo"
		/>
	  <FileFormatSelect/>
  </div>
</template>

<script>
import FileName from './FileName.vue'
import FileFormatSelect from './FileFormatSelect.vue'

let nextTodoId = 1

export default {
	components: {
		FileName, FileFormatSelect
	},
  data () {
    return {
			newTodoText: ''
    }
  }
}
</script>
