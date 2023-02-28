<script>
import Employee from "./components/Employee.vue";
export default {
  components: {
    Employee,
  },
};
</script>
<template>
   <Employee name="Edem" surn="Seytumerov" age="18" />
</template>

<style >
.active {
  border: 5px solid green;
}
.valid {
  color: blue;
}
</style>