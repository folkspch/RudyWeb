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

        <div v-html="this.content[0].description"></div>
        <!-- {{this.content[1].description}} -->
    </v-sheet>  
  </div>
      
</template>

<script>
export default {
  data(){
    return{
      content:[
        {
          created_at:"",
          description:"",
          image:""
        }
      ]
      ,

      // mydata:{
      //   title:[],
      //   description:[]
      // }
    }
  },
  methods:{
    API(){
      const options = {
                url: `http://www.server-rudydev.com/admin-project/api/news`,
                method: 'GET',
            }
            this.$axios(options).then(res => {
              
            //store all data
              this.content=res.data
              console.log(this.content)



            //select custom data
              for(var i=0;i<res.data.length;i++){
                this.mydata.title[i]=res.data[i].title
                this.mydata.description[i]=res.data[i].description
              }

              console.log("API connected")
              // console.log(this.mydata.description[2])
              //  this.content=res.data
              // console.log(this.content)
              // console.log("connected API")
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