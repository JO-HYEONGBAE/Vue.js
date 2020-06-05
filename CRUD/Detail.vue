<template>
    <div>
        <div>{{data.writer}}</div>
        <div>{{data.title}}</div>
        <div>{{data.content}}</div>
        <button @click="updateData(index)">수정</button>
        <button @click="deleteData(index)">삭제</button>
    </div>
</template>

<script>
import data from '@/data'
export default {
    name:'Detail',

    data(){
        const index = this.$route.params.contentId
        return{
            data: data[index],
            index:index
        }
    },
    methods:{
        deleteData(index){
            data.splice(index,1); 
            this.$router.push({
                path:'/'
            }) 
        },
        updateData(index){
            this.$router.push({
                path:"/create/"+index
            })
        }
    }
}
</script>
