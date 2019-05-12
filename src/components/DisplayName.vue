<template>
    <div class="card">
        <div class="card-body">
            <h5 class="card-title">Display User</h5>
            <p class="card-text">Reversed Name is {{reversedName}}.</p>
            <a href="#" class="btn btn-primary btn-sm" @click="resetName" >Reset Name</a>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        displayName: {
            type: String
        }
    },
    methods: {
        resetName: function () {
            this.displayName = "dAcOIt"
            this.$emit('nameWasReset',this.displayName)
        }
    },
    computed: {
        reversedName: function () {
            return this.displayName.split("").reverse().join("")
        }
    }
}
</script>
