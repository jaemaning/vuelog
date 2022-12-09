<template>
    <div class="mt-3">
        <h3>상세페이지</h3>
        <h5>{{data[$route.params.id].title}}</h5>
        <p>{{data[$route.params.id].content}}</p>
        <router-view></router-view>
    </div>
</template>

<script>
export default {
    name : 'Detail',
    components : {

    },
    props:{
        data : Array,
    }
} // vue route -4 참고하기
</script>

<style>

</style>