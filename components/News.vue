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
        <p class="headertxt">{{newsHeader}}</p>
        <v-divider/>
        <v-card-text>
            <a @click="gotoNews(id)">อ่านเพิ่มเตืม</a> 
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
    margin-left: 0.8em;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;

    /* text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
    width: 250px; */
}

</style>