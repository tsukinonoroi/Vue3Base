<script>

import Employee from './components/Employee.vue'
import EmployeeForm from './components/EmployeeForm.vue'
export default {
  data() {
    return {
      developers: [
        {
          id: 1,
          name: 'Edem',
          surn: 'Seytumerov'
        },
        {
          id: 2,
          name: 'Alie',
          surn: 'Asanova'
        },
        {
          id: 3,
          name: 'Farruh',
          surn: 'Ybiica'
        },
      ],
    }
  },
  components: {
    Developer, EmployeeForm
  },
  methods: {
    add(name, surn){
      let id = this.developers.length + 1;
      this.developers.push({
        id, name, surn
      });
    }
  }
}
</script>


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