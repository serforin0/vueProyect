<template>
  <div class="customer-list">
      <div class="data">
          <table class="ui celled table">
              <thead>
                  <tr>
                      <th style="width: 50px; text-align: center">#</th>
                      <th>Name</th>
                      <th>Contry</th>
                      <th style="width: 148;">Action</th>
                  </tr>
              </thead>

              <tbody>
                  <Customer v-for="customer in customers" 
                  :key="customer.id"
                  :customer="customer"
                   />
              </tbody>
          </table>
      </div>
    
  </div>
</template>

<script>
import Customer from "./Customer.vue";

export default {
    name: "CustomerList",
    components: {
        Customer
    },
    props: {
        customers: {
            type: Array
        }
    }

}
</script>

<style scoped>

</style>
