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
            this.age = this.getRandomInt(20, 30)
            this.$emit('ageWasEdited', this.age)
        },
        getRandomInt: function (min, max) {
            min = Math.ceil(min);
            max = Math.floor(max);
            return Math.floor(Math.random() * (max - min)) + min;
        } 
    }
}
</script>
