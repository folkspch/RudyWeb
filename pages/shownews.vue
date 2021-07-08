<template>
  <div>
    <v-sheet light>
        <div class="news-title">
            <h2>หัวข้อข่าว</h2>
            <p style="font-size:50%; color:#666666;">วันที่ 01/01/2021</p>
        </div>
        <v-divider></v-divider>
        <img class="NewsImg" src="../assets/pic.jpg"/>    
        <h3>ใจความสำคัญ</h3>
        {{this.content[1].description}}
    </v-sheet>  
  </div>
      
</template>

<script>
export default {
  data(){
    return{
      content:{}
    }
  },
  methods:{
    API(){
      const options = {
                url: `http://www.server-rudydev.com/admin-project/api/news`,
                method: 'GET',
            }
            this.$axios(options).then(res => {
               this.content=res.data
              console.log(this.content)
            })
    }
  },
  mounted(){
    this.API()
  }
  
}

</script>

<style scoped>
*{
    color:black;
    margin: 1%;
}
.news-title{
    font-size:2em;
}
.NewsImg{
  border: 1px solid black;
}
</style>