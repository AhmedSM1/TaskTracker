<template>
    <header>
       <h2>  {{  title  }} </h2>

     <Button @show-form="$emit('show-form')"
      :text="showAddTask ? 'Close' : 'Add task' "  
      :color="showAddTask ? 'red' : 'green' " />
 </header>
</template>

<script>
import Button from "./Button.vue"
export default {
  name: "Header",
  props: {
      title: String,
      showAddTask: Boolean
  },
  components: {
      Button,
  }
}

</script>

<style scoped>

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.h2 {
   align-items: center;
}

</style>