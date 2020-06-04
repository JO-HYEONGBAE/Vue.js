<template>
  <div class="about">
    <h1>This is an about page</h1>
  <Cho title="About Title" :name1= "name"></Cho>
  </div>
</template>

<script>
import Cho from '@/components/cho.vue';

export default {
  components:{
    Cho
  },
  data(){ 
        return{

            name: 'KIM'
        }

    }
}
</script>
