<template>

<div>
    <div v-for="(dat,i) in data" :key="i">
        <h5>{{dat.title}}</h5>
        <p>{{dat.date}}</p> 
    </div>
</div>

</template>

<script>
export default {
    name : 'List',
    props : {
        data : Array
    },
    components:{

    }
}
</script>

<style>

</style>