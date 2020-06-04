<template>
<div>
    <label for="">Name</label>
         <input type="text" v-bind:value="name" style="padding:30px; border:2px solid blue"
         v-on:input="updateName">
         <br>
         <button>Submit</button>
</div>
    
</template>

<script>
export default {
    props:{
        name:{
            type:String 
        }
    },
    methods:{
        updateName(e){
            console.log(e.target.value);
            this.$emit('update-name',e.target.value);
             this.$emit('update-name2',e.target.value);

        }

    }
}
</script>
