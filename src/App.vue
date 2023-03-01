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
      alert(name);
    },
    developerSalary(salary) {
      alert(salary)
    }
  }
}
</script>

<template>
<Employee @morgen="developerName"/>
<Employee @morgen="developerSalary"/>

</template>

<style >
.button {
    background-color: lightskyblue; 
    border-radius: 16px;
    border: none;
    color: rgb(0, 0, 0);
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    -webkit-transition-duration: 0.4s;
    transition-duration: 0.4s;
}
.active {
  border: 5px solid green;
}
.valid {
  color: blue;
}
</style>