<template>
  <div class="task-grid">
    <template v-if="tasks.length">
        <task v-for="task in tasks" :key="task.name" :task="task"></task>
    </template>
    <p v-else class="no-task">Sua vida está em dia :)</p>
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
    .task-grid {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 10px;
    }
    .no-task {
        color: #aaa;
        font-size: 1.7rem;
    }
</style>