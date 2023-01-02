<template>
  <div class="container">

     <div class="col-md-4">
       <h4>All Employee List</h4>
       <table class="table table-bordered">
         <tr>
            <td>Id</td>
            <td>Name</td>
            <td>Status</td>
         </tr>

         <tr v-for="item in AllEmployeList" :key="item.id">
            <td>{{item.id}}</td>
            <td>{{item.name}}</td>
            <td>{{item.status}}</td>
         </tr>
       </table>
     </div>

     <div class="col-md-4">
       <h4>Active Employee List</h4>
         <table class="table table-bordered">
         <tr>
            <td>Id</td>
            <td>Name</td>
            <td>Status</td>
         </tr>

          <tr v-for="item in activeEmployee" :key="item.id">
            
            <td>{{item.id}}</td>
            <td>{{item.name}}</td>
            <td>{{item.status}}</td>
         </tr>
       </table>
     </div>

     <div class="col-md-4">
         <h4>Inactive Employee List</h4>
         <table class="table table-bordered">
         <tr>
            <td>Id</td>
            <td>Name</td>
            <td>Status</td>
         </tr>

          <tr v-for="item in inactiveEmployee" :key="item.id">
            <td>{{item.id}}</td>
            <td>{{item.name}}</td>
            <td>{{item.status}}</td>
         </tr>
       </table>
     </div>

  </div>
</template>

<style>
table tr td{
  border:1px solid #000000;
}
</style>

<script>
export default {
  props: {
    AllEmployeList:[],
  },
  computed: {
  activeEmployee: function () {
    return this.AllEmployeList.filter(i => i.status === 'Active')
  },
  inactiveEmployee: function () {
   return this.AllEmployeList.filter(i => i.status === 'Inactive')
  }
}
}
</script>

 