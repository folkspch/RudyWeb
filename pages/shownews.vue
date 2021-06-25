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
        <p>เนื่อหาทั้งหมดของข่าว................</p>
    </v-sheet>  
  </div>
      
</template>

<script>
export default {

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