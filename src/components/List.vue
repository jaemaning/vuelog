<template>

<div>
    <div v-for="(dat,i) in data" :key="i">
        <h5 @click="$router.push('/detail/'+i)">{{dat.title}}</h5>
        <p @click="$router.push('/detail/'+i)">{{dat.date}}</p> 
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