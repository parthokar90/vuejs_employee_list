<template>
     <EmployeeList :allEmployeList="allEmployeList"/>
</template>

<script>
import EmployeeList from './components/EmployeeList.vue'

export default {
  components: {
    EmployeeList
  },
  data(){
    return {
      allEmployeList:[
      {
        id:'001',
        name:'Tanveer Vaia',
        status:'Active',
      },
      {
        id:'002',
        name:'Morsalin Vaia',
        status:'Active',
      },
      {
        id:'003',
        name:'Partho',
        status:'Inactive',
      }, 
      {
        id:'004',
        name:'Khadiza Apu',
        status:'Inactive',
      }, 
      ],
    }
  }
}
</script>
