<template>
  <div class="my-direction">
      <form class="ui form">
          <div class="fields">
              <div class="four wide field">
                  <label>First Name</label>
                  <input type="text" name="first_name" placeholder="First Name" />
              </div>

               <div class="four wide field">
                  <label>Last Name</label>
                  <input type="text" name="last_name" placeholder="Last Name" />
              </div>

               <div class="six wide field">
                  <label>Contry Name</label>
                  <input type="text" name="contry_name" placeholder="Contry Name" />
              </div>

              <div class="two wide field">
                  <button class="ui primary button submit-button">Save</button>
              </div>
          </div>

      </form>
      </div>
</template>

<script>
export default {
    name: "MyDirection"
}
</script>

<style scoped>

</style>
