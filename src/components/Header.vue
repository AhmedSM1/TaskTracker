<template>
    <header>
         {{  title  }}
    </header>
     <Button text = "add" color = blue />
     <Button text = "delete" color = red />
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
</style>