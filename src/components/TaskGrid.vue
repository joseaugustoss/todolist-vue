<template>
  <div class="task-grid">
    <template>
        <task v-for="task in tasks" :key="task.name" :task="task"></task>
    </template>
  </div>
</template>

<script>
import Task from '@/components/Task.vue'
export default {
    props:{
        tasks: {type: Array, required: true}
    },
    components: {
        Task
    }
}
</script>

<style>

</style>