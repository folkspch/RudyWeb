<template>
<div>
    <div class="carousel">
        <v-carousel class="carousel"
        id="slider"
        cycle
        height="500"
        hide-delimiter-background
        show-arrows-on-hover
      >
        <v-carousel-item v-for="(pics, i) in pic" :key="i">
          <v-img class="rdy_image" :src="pic[i]"/> 
        </v-carousel-item>
      </v-carousel>
    </div>
    <div>
      <AboutRudy/>
    </div>
    <!-- <v-responsive>
     <v-card light>
        <v-card-title >
            <div id="AboutRudy-title"> About RUDY</div>
        </v-card-title>
        <v-card-text id="AboutRudy-text">    
            
                Rudy แอพพลิเคชั่นบริหารการขายผ่านระบบคลาวด์ เพื่อเพิ่มประสิทธิภาพการขายที่ไซต์งาน
                ประเมินโอกาสขายในแต่ละเฟสงานก่อสร้าง เตือนการติดตามการขายให้ครบทั้งหลัง
                เข้าถึงข้อมูลได้ทุกที่ทุกเวลา ช่วยงานบริหารทีมขายอย่างมืออาชีพ
            
        </v-card-text>
    </v-card>
    </v-responsive> -->
    

  <div class="News-container">
    <div class="titleNews-container">
      <v-row>
        
        <img src="../assets/rudyPic/rdylogo.png" height="70em" width="140em" />
        <div class="NewsTitleText">NEWS</div>
        
      </v-row>
    </div>  
  <v-sheet
    class="mx-auto"
    max-width="60%"
    light
  >
    <v-slide-group
      
      show-arrows
    >
      <v-slide-item
        v-for="n in 10"
        :key="n"
      >
      <News class="Ex-news"/>
      
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
  </div>
</div>
  
</template>

<script>
import News from '@/components/News'
import AboutRudy from '@/components/aboutRudy'

export default {
  data(){
    return{
    model:null,
      pic:[
    "https://thestandard.co/wp-content/uploads/2018/09/ADVER-SCG_COVER.jpg",
    "https://www.jobbkk.com/upload/employer/0C/2CC/02D2CC/images/2019-08-136097.jpg",
    "https://scontent.fbkk5-1.fna.fbcdn.net/v/t1.6435-9/124373500_203637101174661_3976716168331546315_n.jpg?_nc_cat=109&ccb=1-3&_nc_sid=730e14&_nc_eui2=AeEvUwCnpbEKxUTJWMNWDABv2SRmwuB6r5DZJGbC4HqvkBGf_-bP14AsulOxKidMpk75Pb-00CSl2BhWJN3j0bQQ&_nc_ohc=p84bYY8_nXEAX-hnu9H&_nc_ht=scontent.fbkk5-1.fna&oh=24accb05d0ade07495b106f9a41f22a0&oe=60D6159F"
  ],
    }
  },
  components:{
    News,
    AboutRudy
    
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Prompt:wght@100;300;500&display=swap');
*{
  color: black;
  justify-content: center;
  align-items: center;
  font-family: 'Prompt', sans-serif;
}
.container{
  margin-top: 0%;
  padding: 0%;
}
#main{
  background-color: white;
}
.carousel{
  padding: 0em;
  width:100%;
}
.rdy_image{
  width: 100%;
  
}
#text{
  color: black;
  
}
.AboutRudy-text{
  text-align: center;
  justify-content: center;
  align-items: center;
}
#rdyImg{
  width:5em;
  height:2.5em;
  margin-top: 1em;
}
.News-container{
  margin:4%;
  
}
.NewsTitleText{
  font-size: 2em;
  margin-left:5px;
  font-style: normal;
  
}
.titleNews-container{
  margin-bottom: 4%;
}
</style>
