<template>
  <div id="app">
    <div class="ui fixed inverted menu vue-color">
      <div class="ui container">
        <a href="#" class="header item">Vue JS CRUD with API</a>
      </div>
    </div>

    <div class="ui main container">
      <MyDirection />
      <CustomerList :customers="customers" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import MyDirection from "./components/MyDirection.vue";
import CustomerList from "./components/CustumerList.vue";

export default {
  name: "App",
  components: {
    MyDirection,
    CustomerList,
  },
  data() {
    return {
      url: "https://my-json-server.typicode.com/serforin0/demo/data",
      customers: [],
    };
  },
  methods: {
    getCustomerts() {
      axios.get(this.url).then((data) => {
        this.customers = data.data;
      });
    },
  },
  created() {
    this.getCustomerts();
  },
};
</script>

<style>
.vue-color {
  background: #41b883 !important;
}
.main.container {
  margin-top: 60px;
}

.submit-button {
  margin-top: 24px !important;
  float: right;
}
</style>
