<template>
     <div id="app" class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="jumbotron">
              <h1 class="display-5"> Parent to Child Demo</h1>
              <p>User name is : {{ name }}</p>
              <p class="lead">
                <a class="btn btn-success btn-md" href="#" @click="changeName" role="button">Change Name</a>
              </p>
            </div>
          </div>
          <div class="col-lg-6">
              <display-name :display-name="name" @nameWasReset="name= $event" :displayAge=age></display-name>
          </div>
          <div class="col-lg-6">
              <edit-age :age="age" @ageWasEdited="age= $event"></edit-age>
          </div>
        </div>
    </div>
</template>

<script>

import DisplayName from './components/DisplayName.vue'
import EditAge from './components/EditAge.vue'

export default {
  data: function () {
    return {
      name: "Janardhan",
      age: 33
    }
  },
  methods: {
    changeName: function () {
      this.name = "Janardhan Maithil"
    }
  },
  components: {
    'display-name': DisplayName,
    'edit-age': EditAge
  }
}
</script>

<style scoped>
  div{
    border: 2px solid rgb(red, green, blue)
  }
</style>
