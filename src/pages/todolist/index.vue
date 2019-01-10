<template>
    <div>
      hello
      <ToDoList></ToDoList>
    </div>
</template>

<script>
  import ToDoList from '@/components/ToDoList'
  export default {
    name: 'index',
    components: {
      ToDoList
    }
  }
</script>

<style scoped>

</style>
