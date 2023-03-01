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
    handle() {
      alert('c++ is hard for me');
    },
    handle1(){
      alert('i like python')
    }
  }
}
</script>

<template>
<Employee @show="prikolovni" @show1="bebrusovi" />
</template>

