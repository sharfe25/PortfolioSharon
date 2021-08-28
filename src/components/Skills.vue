<template>
<v-card
    id="skills"
    tile
    color="#1D1D1D"
    elevation="0" 
    class="d-flex justify-center cardSkills d-flex skillsText pb-5"
>
    <v-card elevation="0" color="transparent"  class="pt-6 text-center cardSkill pb-5" shaped rounded style="width:85%;">
        <v-row
        class="pt-3 px-3"
        >
        <v-col
            cols="12"
            lg="6"
            md="6"
            sm="12"
            xl="6"
        >
            <v-card-text class="titleSkills pt-2 pl-5 text-start">
            My Skills
            </v-card-text>
            <v-card-text class="pt-7 text-start pl-5 white--text">
                I create a successful responsive websites that are fast, easy to use, and built with best practices. The main are of my expertise is front-end development, HTML, CSS, JS building small and medium web apps, custom plugins, features, animations, and coding interactive layouts.
                I also hace full-stack developer experience with popular open-source CMS like Wordpress.
                Visit my Linkedln profile for more details or just contact me.
            </v-card-text>
        </v-col>
        <v-col
            cols="12"
            lg="6"
            md="6"
            sm="12"
            xl="6"
        >
            <div class="mx-6 pt-7">
                <v-card-text class="px-0 pb-1 text-start white--text skill">
                Frontend
                </v-card-text>
                <v-progress-linear
                value="60"
                color="rgb(70, 159, 241)"
                ></v-progress-linear>
                <br>
                <v-card-text class="px-0 py-0 pb-1 text-start white--text skill">
                Backend
                </v-card-text>
                <v-progress-linear
                value="40"
                color="rgb(115, 56, 226)"
                ></v-progress-linear>
                <br>
                <v-card-text class="px-0 py-0 pb-1 text-start white--text skill">
                Mobile
                </v-card-text>
                <v-progress-linear
                value="20"
                color="#FD2155"
                ></v-progress-linear>
            </div>
        </v-col>
        </v-row>
        <v-row
        class="pt-3 px-3"
        align="center"
        justify="center"
        >
            <v-col
                cols="6"
                lg="3"
                md="3"
                sm="6"
                xl="3"
                :key="skill"
                v-for="skill in skillsImages"
            >
                <div class="mx-6 d-flex justify-center">
                    <v-img 
                        :src="getImg(skill)"
                        alt="logo"
                        max-width="100"
                        height="100"
                        contain
                    >
                    </v-img>
                </div>
            </v-col>
        </v-row>
    </v-card>
</v-card>
</template>

<script>
  export default {
    name: 'Skills',

    components: {
      
    },
    data () {
        return{
            skillsImages: [
                'css.png','javaScript.png','nodeJs.png','react.png','vue.png','wordpress.png','angular.png','mysql.png'
            ],
        }
    },
    methods:{
        getImg(name){
            if (typeof name != 'undefined') {
                return require('../assets/' + name);
            }
        },
    }
  }
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@300;600&display=swap');
.skillsText{
    font-family: 'Raleway', sans-serif !important; 
}
.titleSkills{
    color:rgb(70, 159, 241) !important;
    letter-spacing:3px;
    font-weight:800 !important;
    font-size: calc(2em + 2vw) !important;
}
.skill{
    font-weight:600;
    letter-spacing:3px;
}
.cardSkill{
    border: 1px solid white !important;
    border-radius:10px !important;
}
</style>