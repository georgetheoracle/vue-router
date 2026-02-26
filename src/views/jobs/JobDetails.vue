<template>
  <h1>{{jobs?.title}}</h1>
  <p>The job id is {{ id }}.</p>
    <p>{{ jobs?.details }}</p>
</template>

<script>
export default {
    props: ['id'],
    data(){
        return{
            jobs: null
        }
    },
    mounted(){
        fetch('http://localhost:3000/jobs/' + this.id)
        .then(res => res.json())
        .then(data => this.jobs = data)
        .catch(err => console.log(err.message))
    }

}
</script>

<style>

</style>