<template>
<div >
  <div class="main-container">
    <h2>CEO</h2>
    <v-row>
      <div class="CeoProfile-container"
      v-for="n in this.person.CEO.length"
        :key="n" >
          <Profile :name="person.CEO[n-1]" position="CEO" img="https://innova-it.co.il/wp-content/uploads/2018/12/bg.jpg" />
      </div>
    </v-row>
     <h2>Frontend</h2>
    <v-row>
      <div class="DevProfile-container"
      v-for="n in this.person.Dev.Frontend.length"
        :key="n" >
          <Profile :name="person.Dev.Frontend[n-1]" position="Frontend Developer" img="https://www.cstcloud.net/r/cms/cstclouden/default/images/bg.png" />
      </div>
    </v-row>
     <h2>Backend</h2>
    <v-row>
      <div class="DevProfile-container"
      v-for="n in this.person.Dev.Backend.length"
        :key="n" >
          <Profile :name="person.Dev.Backend[n-1]" position="Backend Developer" img="https://cdn.vuetifyjs.com/images/cards/server-room.jpg" />
      </div>
    </v-row>
     <h2>Project Manager</h2>
    
    <v-row>
      <div class="DevProfile-container"
      v-for="n in this.person.PM.length"
        :key="n" >
          <Profile :name="person.PM[n-1]" position="Project Manager" img="https://img.freepik.com/free-vector/flowing-speed-lines-technology-background_1017-31772.jpg?size=626&ext=jpg"/>
      </div>
    </v-row>
  </div>
</div> 
</template>

<script>
import Profile from '@/components/Profile'
export default {
  data(){
    return{
        person:{
          CEO:["CEO A"],
          Dev:{
            Frontend:["FE A","FE B","FE C"],
            Backend:["BE A","BE B","BE C"]
          },
          PM:["PM A","PM B"]

        }
    }
  },
  components:{
    Profile
  },
  

}
</script>

<style scoped>
.main-container{
  display: grid;
  justify-content: center;
  padding: 1em;
}
.CeoProfile-container{
  padding-bottom: 1.5em;
}
.DevProfile-container{
  padding-bottom: 1.5em;
}
h2{
  color: black;
}
</style>