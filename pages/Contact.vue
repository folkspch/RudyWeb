<template>
<div>
    <v-row class="map-container"> 
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3874.292579341155!2d100.53283621483125!3d13.821461890302388!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30e29d13dcf2cda9%3A0x41b386b9040a6f3d!2sRudy%20House!5e0!3m2!1sth!2sth!4v1624448747880!5m2!1sth!2sth" 
        width="1000" height="600" style="border:0;" allow="fullscreen" loading="lazy" class="map"></iframe>
        <v-card light class="address">
            <v-card-title class="tile-address">ที่อยู่ของเรา</v-card-title>
            <v-card-text><div class="text-address">Rudy House ซอย กรุงเทพ-นนทบุรี 36 แขวง บางซื่อ เขตบางซื่อ กรุงเทพมหานคร 10800 </div></v-card-text>
            <v-divider></v-divider>

            <v-card-title class="tile-tel">เบอร์โทร</v-card-title>
            <v-card-text><div class="text-tel"> 096-1915246</div></v-card-text>
            <v-divider></v-divider>

            <v-card-title class="tile-tel">Social</v-card-title>
            <div class="social-btn">
                <a href="https://www.facebook.com/rudytechnology/"><img src="../assets/fblogo.png" width="60px" height="60px"/></a>
                <a href="https://page.line.me/upt6090o?openQrModal=true"><img src="../assets/linelogo.png" width="60px" height="60px"/></a>
                
            </div>
            <v-divider></v-divider>
        </v-card>
    </v-row>
</div>
</template>

<script>
export default {

}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Prompt:wght@100;300;500&display=swap');
    *{
        font-family: 'Prompt', sans-serif;
    }
    .map{
        margin: 1em;
    }
    .address{
        margin: 1em;
    }
    .map-container{
        margin: 0.5em;
    }
    .social-btn{
        margin-left: 1em;
        margin-bottom: 0.8em;
    }

</style>