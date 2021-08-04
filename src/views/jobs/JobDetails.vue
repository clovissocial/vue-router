<template>
    <h1>Job Details Page</h1>
    <p>The Job id is {{ title }}</p>
</template>

<script>
export default {
    props: ['id'], //Accepting the route parameter as a prop
    // data() {
    //     return {
    //         id: this.$route.params.id
    //     } 
    // }
}
</script>

<style lang="css">
    
</style>