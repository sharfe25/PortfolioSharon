<template>
<v-card
    id="about"
    tile
    color="#1D1D1D"
    elevation="0" 
    class="d-flex justify-center cardSkills d-flex skillsText pb-5"
>
    <v-card elevation="0" color="transparent"  class="pt-6 text-center" shaped rounded style="width:85%;">
        <v-row
        class="pt-6 px-3"
        >
            <v-col
                cols="12"
                lg="6"
                md="6"
                sm="12"
                xl="6"
            >
                <v-img 
                        src="../assets/developer.png"
                        alt="logo"
                        max-width="2000"
                        max-height="2000"
                        contain
                    >
                    </v-img>
            </v-col>
            <v-col
                cols="12"
                lg="6"
                md="6"
                sm="12"
                xl="6"
            >
                <v-card-text class="titleSkills pt-2 pl-5 text-end">
                About
                </v-card-text>
                <v-card-text class="pt-7 text-end pl-5 white--text textAbout">
                I'm a Front-End developer located in Colombia. I have a serious passion for UI effects, animations and creating intuitive, dynamic user experiences.
                <br>
                Well-organized person, problem solver, independent employee with high attention to detail.
                <br>
                Interested in the entire frontend spectrum and working on ambitious projects with posetive people.
                <br>
                Let's make something special.
            </v-card-text>
            </v-col>
        </v-row>
    </v-card>
</v-card>
</template>

<script>
  export default {
    name: 'About',

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
    color:rgb(115, 56, 226) !important;
    font-weight:700 !important;
    font-size:5rem;
    border-bottom: 1px solid white;
    padding-bottom: 2rem;
}
.skill{
    font-weight:600;
    letter-spacing:3px;
}
.textAbout{
    font-size:1rem;
}
</style>