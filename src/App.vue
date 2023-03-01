<script>
import Employee from './components/Employee.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    Employee
  },
  methods: {
    developerName(name) {
      console.log(name);
    },
    developerSalary(name, salary){
console.log(name, salary);
    }
  }
}
</script>

<template>
<Employee @show="morgen" @show1="morgen1" />
</template>

