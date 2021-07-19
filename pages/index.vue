<template>
  <div>
    <div class="carousel">
      <v-carousel
        class="carousel"
        id="slider"
        cycle
        height="500"
        hide-delimiter-background
        show-arrows-on-hover
      >
        <v-carousel-item v-for="item in picAPI" :key="item.image">
          <v-img class="rdy_image" :src="item.image" />
        </v-carousel-item>
      </v-carousel>
    </div>
    <div>
      <AboutRudy class="AboutRudy" />
    </div>
    <div class="News-container">
      <div class="titleNews-container">
        <v-row>
          <img
            src="../assets/rudyPic/rdylogo.png"
            height="70em"
            width="140em"
          />
          <div class="NewsTitleText">NEWS</div>
        </v-row>
      </div>
      <v-sheet class="mx-auto" max-width="60%" light>
        <v-slide-group show-arrows>
          <v-slide-item v-for="n in this.newsAPI.length" :key="n">
            <News
              class="Ex-news"
              :newsHeader="newsAPI[n - 1].title"
              :image="newsAPI[n - 1].image"
              :id="n"
            />
          </v-slide-item>
        </v-slide-group>
      </v-sheet>
    </div>
  </div>
</template>

<script>
import News from "@/components/News";
import AboutRudy from "@/components/aboutRudy";

export default {
  data() {
    return {
      model: null,
      picAPI: {},
      newsAPI: [
        {
          image: "",
          title: "",
        },
      ],
    };
  },
  components: {
    News,
    AboutRudy,
  },
  methods: {
    APIbanner() {
      const options = {
        url: `http://www.server-rudydev.com/admin-project/api/banner`,
        method: "GET",
      };
      this.$axios(options).then((res) => {
        this.picAPI = res.data;
        //  console.log(this.picAPI)
      });
    },
    APInews() {
      const options = {
        url: `http://www.server-rudydev.com/admin-project/api/news`,
        method: "GET",
      };
      this.$axios(options).then((res) => {
        this.newsAPI = res.data;
        console.log(this.newsAPI);
      });
    },
  },

  mounted() {
    this.APIbanner();
    this.APInews();
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Prompt:wght@100;300;500&display=swap");
* {
  color: black;
  justify-content: center;
  align-items: center;
  font-family: "Prompt", sans-serif;
}
.container {
  margin-top: 0%;
  padding: 0%;
}
#main {
  background-color: white;
}
.carousel {
  padding: 0em;
  width: 100%;
}
.AboutRudy {
  margin-bottom: 10%;
}
.rdy_image {
  width: 100%;
}
#text {
  color: black;
}
.AboutRudy-text {
  text-align: center;
  justify-content: center;
  align-items: center;
}
#rdyImg {
  width: 5em;
  height: 2.5em;
  margin-top: 1em;
}
.News-container {
  margin: 4%;
}
.NewsTitleText {
  font-size: 2em;
  margin-left: 5px;
  font-style: normal;
}
.titleNews-container {
  margin-bottom: 3%;
}
</style>
