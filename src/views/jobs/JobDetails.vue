<template>
    <div v-if="job">
        <h1>{{ job.title }}</h1>
        <p>The Job id is {{ id }}</p>
        <p>The Job Title is: {{ job.details }}</p>
    </div>
    <div v-else>
        <p>Job Details loading...</p>
    </div>
</template>

<script>
export default {
    props: ['id'], //Accepting the route parameter as a prop
    // data() {
    //     return {
    //         id: this.$route.params.id
    //     } 
    // }

    data() {
        return {
            job: null
        }
    },

    mounted() {
         fetch('http://localhost:3000/jobs/' + this.id)
        .then((res) => res.json())
        .then(data => this.job = data)
        .catch(err => console.log(err.message))
    }
}
</script>

<style lang="css">
    
</style>