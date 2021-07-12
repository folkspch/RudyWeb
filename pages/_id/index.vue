<template>
  <div>
    <v-sheet light>
        <div class="news-title">
            <h2>{{this.data.title}}</h2>
            <p style="font-size:50%; color:#666666;">{{this.data.created_at}}</p>
        </div>
        <v-divider></v-divider>
        <div v-html="this.data.description"></div>
    </v-sheet>  
  </div>
      
</template>

<script>
export default {
  data(){
    return{
        id: this.$route.params.id,
        data: "",
    }
  },
  methods:{
    API(){
      const options = {
                url: `http://www.server-rudydev.com/admin-project/api/news/${this.id}`,
                method: 'GET',
            }
            this.$axios(options).then(res => {
              
            //store all data
                this.data=res.data
                console.log(this.data)
                console.log("API connected")

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