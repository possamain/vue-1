<template>
	<div>
		<select v-if="formats.length" v-model="selected">
    <option v-if="format" v-for="format in formats" value="json">{{ format.text }}</option>
			
		</select>
	</div>
</template>

<script>
import FileFormatOption from './FileFormatOption.vue'

let nextFormatId= 1

export default {
	components: {
		FileFormatOption
	},
  data () {
    return {
			selected: -1,
      formats: [
				{
					id: nextFormatId++,
          value: 'json',
					text: 'json'
				},
				{
					id: nextFormatId++,
          value: 'csv',
					text: 'csv'
				},
				{
					id: nextFormatId++,
          value: 'xls',
					text: 'xls'
				}
			]
    }
  }/*,
	methods: {
		addTodo () {
			const trimmedText = this.newTodoText.trim()
			if (trimmedText) {
				this.todos.push({
					id: nextTodoId++,
					text: trimmedText
				})
				this.newTodoText = ''
			}
		},
		removeTodo (idToRemove) {
			this.todos = this.todos.filter(todo => {
				return todo.id !== idToRemove
			})
		}
	}*/
}
</script>