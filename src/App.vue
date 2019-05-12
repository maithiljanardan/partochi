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
              <display-name :display-name="name" @nameWasReset="name= $event"></display-name>
          </div>
          <div class="col-lg-6">
            
          </div>
        </div>
    </div>
</template>

<script>

import DisplayName from './components/DisplayName.vue'

export default {
  data: function () {
      return {
        name: "Janardhan"
      }
    },
    methods: {
      changeName: function () {
        this.name = "Janardhan Maithil"
      }
    },
    components: {
      'display-name' : DisplayName
    }
}
</script>

<style scoped>
  div{
    border: 2px solid rgb(red, green, blue)
  }
</style>
