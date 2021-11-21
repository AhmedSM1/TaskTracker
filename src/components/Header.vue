<template>
    <header>
       <h2>  {{  title  }} </h2>
    </header>
     <Button @show-form="$emit('show-form')" text = "add" color = blue />
     
</template>

<script>
import Button from "./Button.vue"
export default {
  name: "Header",
  props: {
      "title": String
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