<template>
   <div :key="task.id" v-for="task in tasks" >
      
       <Task  
       @toggle-reminer="toggleReminder(task.id)"
       @delete-task="deleteTask(task.id)"
       :task="task" />
   </div>
</template>

<script>
import Task from './Task.vue';
export default {
    
    name: 'Tasks',

    props: {
        tasks: Array
    },
    components: {
        Task,
    }, 
    methods: {
       deleteTask(id){
        this.$emit('delete-task', id);
        }, 
        toggleReminder(id){
          this.$emit('toggle-reminder', id)
        }
    }, 
    emits: ['delete-task', 'toggle-reminder']


}
</script>