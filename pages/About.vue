<template>
<div>
  <v-row>
    <div
    v-for="n in this.name.length"
      :key="n" >
        <Profile :name="name[n-1]" :position="position[n-1]" />
    </div>
  </v-row>  
</div> 
</template>

<script>
import Profile from '@/components/Profile'
export default {
  data(){
    return{
        name:[
          'A','B','C','D'
        ],
        position:[
          "CEO","Fronend Dev","Backend Dev","Project Manager"
        ]
    }
  },
  components:{
    Profile
  },
  

}
</script>

<style scoped
  
</style>