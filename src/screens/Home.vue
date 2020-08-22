<template>
   <scroll-view :content-container-style="{contentContainer: {
        paddingVertical: 20
    }}">
     <text class="container" v-for="todo in todos" :key="todo.id">
    {{ todo.title }}
  </text>
        <!-- Content goes here -->
    </scroll-view>
</template>
<script>
import Vue from 'vue-native-core'
//Vue.store.prototype.$store = store
export default {
  
}
</script>
<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
<script>
  import axios from 'axios'
  export default {
    data () {
      return {
        title: 'Home Screen!'
      }
    },
    created () {
      this.$store.dispatch('fetchTodos')
    },
    computed: {
      // 5. Get todos from state
      todos () {
        return this.$store.state.todos
      }
    },
  }
</script>