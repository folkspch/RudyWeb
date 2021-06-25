<template>
<div>
    
    <div>
    <v-card class="Ex-news"
    max-width="300"
    light
    color="#efefef">
        <img
        height="200"
        width="200"
        src="../assets/rudyPic/rdylogo_w.jpg"
        />
        <v-card-title>ตัวอย่างข่าว</v-card-title>
        <v-card-text> 
            <v-row
                align="center"
                class="mx-0">
                <div class="news-content">เนื้อหาของข่าว</div>
            </v-row>
        </v-card-text>
        <v-card-text>
            <Nuxt-link to="/shownews">
                อ่านเพิ่มเติม..
            </Nuxt-link>    
        </v-card-text>    
    </v-card>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style scoped>
.Ex-news{
    margin: 0.7em;
}
</style>