<template>
<div>
    
    <div>
    <v-card class="Ex-news"
    max-width="300"
    light
    color="#efefef">
        <img
        height="200"
        width="300"
        :src="image"
        />
        <v-card-title class="headertxt">{{newsHeader}}</v-card-title>
        <v-card-text> 
            <v-row
                align="center"
                class="mx-0">
                <div class="news-content">{{title}}</div>
            </v-row>
        </v-card-text>
        <v-divider/>
        <v-card-text>
            <a @click="gotoNews(id)">อ่านเพิ่มเตืม...</a> 
        </v-card-text>    
    </v-card>
    </div>
</div>
</template>

<script>
export default {
    data(){
        return{
            
        }
    },
    methods:{
        gotoNews(id){
            console.log(id)
            // this.$router.push(`shownews/${id}`)
            this.$router.push(`/${id}`)
        }
    },
    props:{
        newsHeader: String,
        title: String,
        image: String,
        id:Number
    }
    
}
</script>

<style scoped>
.Ex-news{
    margin: 0.7em;
}
.headertxt{
    font-size: 100%;
}
</style>