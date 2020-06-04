<template>
    <div>
        <p>{{title}}</p>
        <h1>
            {{name1}}
        </h1>
        <button type="button" v-on:click="updateName">버튼</button>
    </div>

</template>

<script>
export default {
    props:['title','name1'],
    data(){ 
        return{

            name: 'KIM'
        }

    },

    methods:{
        updateName(){
            this.name='CHO'
        }
    }

}
</script>

<style scoped>


</style>
