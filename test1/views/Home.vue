<template>
  <div>
    <h1> 
      This is Home page
    </h1>
    <form>
      <InputField :name="name" @update-name="updateName"  @update-name2="updateName"></InputField>
    </form>
    {{name}}

    <!-- <p>
      {{name}}
    </p>
    <Cho id="s" title="Home Title"></Cho> -->
  </div>
</template>

<script>
// import Cho from '@/components/cho.vue';
import InputField from '@/components/inputField.vue';
export default {
  // components:{ 
  //   Cho
  // },
  components:{
    InputField
  },
  data (){
    return{
      name:"s"
    }
  },
  methods:{
    updateName(name){
      this.name=name ;
    }
  }
}
</script>

<style scoped>
h1{

  color:red
}
#s{
  color:blue
}
</style>
