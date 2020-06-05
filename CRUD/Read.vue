<template>
    <div>
        <table>
            <tr>
                <td>글쓴이</td>
                <td>제목</td>
                <td>내용</td>
            </tr>
             <tr v-for="(data,i) in value" :key="i" @click="detail(i)">
                <td>{{data.writer}}</td>
                <td>{{data.title}}</td>
                <td>{{data.content}}</td>
            </tr>
            
        </table>
        <button @click="write">글쓰기</button>
    </div>
</template>
<script>
import data from '@/data';
export default {
    name:'Read',
    data(){
        return{
            value:data
        }
    },
    methods:{
         write(){
             this.$router.push({
                 path:'create'
             })
         },
         detail(index){
            this.$router.push({
               name:'Detail',
               params: {
                   contentId:index
               } 
            })
         }
    } 
}
</script>
