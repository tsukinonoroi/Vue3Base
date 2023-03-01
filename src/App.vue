<script>
import Employee from './components/Employee.vue'
export default {
  data() {
    return {
      humans: [
        {
          id: 1,
          name: 'Edem',
          salary: 1000,
          age: 18
        },
        {
          id: 2,
          name: 'Alie',
          salary: 10000,
          age: 18
        },
        {
          id: 3,
          name: 'Farruh',
          salary: 30003,
          age: 18
        },
      ],
    }
  },
  components: {
    Employee
  }
}
</script>

<template>
<Employee v-for="human in humans" :name="human.name" :salary="human.salary" :age="human.age" :key="human.id" />
</template>