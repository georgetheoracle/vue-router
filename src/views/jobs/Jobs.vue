<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    <h2>{{ job.title }}</h2>
  </div>
</template>

<script>
export default {
data(){
    return{
        jobs:[
            {id:1, title:'Frontend Developer', details:'lorem'},
            {id:2, title:'Backend Developer', details:'lorem'},
            {id:3, title:'Fullstack Developer', details:'lorem'},
        ]
    }
}
}
</script>

<style>

</style>