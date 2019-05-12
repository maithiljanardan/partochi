<template>
    <div class="card h-100">
        <div class="card-body">
            <h5 class="card-title">Edit Age</h5>
            <p class="card-text">Age is {{age}}</p>
            <button class="btn btn-success btn-sm mt-4" @click="editAge">Change Age</button>
        </div>
    </div>
</template>
<script>
export default {
    props: ['age'],
    methods: {
        editAge: function () {
            this.age = 20
            this.$emit('ageWasEdited', this.age)
        }
    }

}
</script>
