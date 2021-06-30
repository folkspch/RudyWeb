<template>
<div class="AboutRudy-container">
    <v-card light>
        <v-card-title>
            <div> About Rudy</div>
        </v-card-title>
        <v-card-text>   
            <div>
                Rudy แอพพลิเคชั่นบริหารการขายผ่านระบบคลาวด์ เพื่อเพิ่มประสิทธิภาพการขายที่ไซต์งาน
                ประเมินโอกาสขายในแต่ละเฟสงานก่อสร้าง เตือนการติดตามการขายให้ครบทั้งหลัง
                เข้าถึงข้อมูลได้ทุกที่ทุกเวลา ช่วยงานบริหารทีมขายอย่างมืออาชีพ
            </div>
        </v-card-text>
    </v-card>
    <div class="Advertise">
        <h1>คุณอาจจะเคยพบปัญหาในการทำตลาดเชิงรุกที่ไซต์งาน เช่น</h1>
        <div class="icon-container">     
            <v-row justify="space-around">
                <div>
                    <v-row>
                        <v-icon
                        color="green darken-2"
                        class="icon"
                        >
                        mdi-bullseye
                        </v-icon>
                        <div class="AdText">
                        <h3>ยอดขายไม่เป็นไปตามแผน </h3>
                        <span>ขาดการติดตามการขายที่ไซต์งาน</span><br/>
                        <span>อย่างต่อเนื่องและเป็นระบบ</span>
                        </div>
                    </v-row>
                </div>

                 <div>
                    <v-row>
                        <v-icon
                        color="blue darken-2"
                        class="icon"
                        >
                        mdi-cog
                        </v-icon>
                        <div class="AdText">
                        <h3>สูญเสียโอกาสในการขาย</h3>
                        <span>ขายเฉพาะสินค้าที่ขายง่าย</span><br/>
                        <span>และมีความเชี่ยวชาญ</span>
                        </div>
                    </v-row>
                </div>

                 <div>
                    <v-row>
                        <v-icon
                        color="yellow darken-2"
                        class="icon"
                        >
                        mdi-table
                        </v-icon>
                        <div class="AdText">
                        <h3>ขาดข้อมูลประกอบการวางแผนและตัดสินใจ  </h3>
                        <span>ข้อมูลหน้างานกระจัดกระจาย</span><br/>
                        <span>ไม่ได้ถูกจัดเก็บอย่างเป็นระบบ</span>
                        </div>
                    </v-row>
                </div>

                <div>
                    <v-row>
                        <v-icon
                        color="orange darken-2"
                        class="icon"
                        >
                        mdi-account
                        </v-icon>
                        <div class="AdText">
                        <h3>ไม่สามารถประเมินประสิทธิภาพ</h3>
                        <span>ไม่สามารถประเมินประสิทธิภาพ</span><br/>
                        <span>ของทีมขายได้อย่างชัดเจน</span>
                        </div>
                    </v-row>
                </div>
            </v-row>
        </div>
        <div>
            <img  class="img-prod" src="../assets/rudy_prod.png">
        </div>
    <div class="Advertise2">
        <h1>เราสามารถช่วยอะไรคุณได้บ้าง</h1>
        <div class="icon-container">     
            <v-row justify="space-around">
                <div>
                    <v-row>
                        <v-icon
                        color="green darken-2"
                        class="icon"
                        >
                        mdi-chart-line
                        </v-icon>
                        <div class="AdText">
                        <h3> เพิ่มประสิทธิภาพการขายที่ไซต์งาน </h3>
                        <span>ประเมินโอกาสขายในแต่ละเฟสงานก่อสร้าง</span><br/>
                        <span>เตือนติดตามการขายให้ครบทั้งหลัง</span>
                        </div>
                    </v-row>
                </div>

                 <div>
                    <v-row>
                        <v-icon
                        color="blue darken-2"
                        class="icon"
                        >
                        mdi-apple-icloud
                        </v-icon>
                        <div class="AdText">
                        <h3>เข้าถึงข้อมูลได้ทุกที่ ทุกเวลา</h3>
                        <span>รายงาน สรุป วิเคราะห์ข้อมูลเชิงลึก</span><br/>
                        <span>เชื่อมต่อกับระบบฐานข้อมูลร้านค้า</span>
                        </div>
                    </v-row>
                </div>

                 <div>
                    <v-row>
                        <v-icon
                        color="yellow darken-2"
                        class="icon"
                        >
                        mdi-account-multiple
                        </v-icon>
                        <div class="AdText">
                        <h3>บริหารทีมขายอย่างมืออาชีพ</h3>
                        <span>ระบบบริหารจัดการทีมขาย</span><br/>
                        <span>สรุปผลการดำเนินงานตามช่วงเวลา</span>
                        </div>
                    </v-row>
                </div>
            </v-row>
        </div>
    </div>
    </div>
</div>
</template>

<script>
export default {
    data(){
        return{

            

        }
    }
}
</script>

<style scoped>
*{
    color: black;
}
.Advertise{
    text-align: center;
    justify-content: center;
    align-items: center;
    margin-top: 5%;
}
.icon{
    margin-top: 4%;
    font-size: 600px;

}
.mdi:before {
    font-size: 100px;
}
.AboutRudy-container{
    margin: 1em;

}
.AdText{
    margin-top: 1.5em;
}
.icon-container{
    margin: 5em;
}
.img-prod{
    margin-top: 5%;
    margin-bottom: 6%;
}

</style>