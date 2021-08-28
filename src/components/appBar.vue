<template>
<div>
    <v-app-bar
      absolute
      class="px-sm-8 px-0 align-center justify-center"
      dark
      
      color="#181818"
    >

        <v-btn v-if="!height" text class="text-capitalize buttonAppBar" href="#skills">
            Skills
        </v-btn>

        <v-btn v-if="!height" text class="text-capitalize buttonAppBar" href="#about">
            About
        </v-btn>
        
        <v-spacer v-if="!height"></v-spacer>

        <v-avatar v-if="!height">
            <v-img 
                src="../assets/logo.png"
                alt="logo"

            >
            </v-img>
        </v-avatar>


      <v-spacer v-if="!height"></v-spacer>

      <v-btn v-if="!height" href="https://www.linkedin.com/in/sharon-rueda-fern%C3%A1ndez-64b2201a7" target="_blank" icon>
        <v-icon>mdi-linkedin</v-icon>
      </v-btn>
        
      <v-btn v-if="!height" href="https://www.instagram.com/sharfe25/" target="_blank" icon class="mr-2">
        <v-icon>mdi-instagram</v-icon>
      </v-btn>

      <v-btn v-if="!height" rounded outlined color="white" href="#contact" class="text-capitalize buttonAppBar">
        Contact me
      </v-btn>
      <v-app-bar-nav-icon v-if="height" @click="mobileMenu=true"></v-app-bar-nav-icon>
    </v-app-bar>
    <v-navigation-drawer
    v-model="mobileMenu"
    absolute
    temporary
    class="background_mobile_menu"
    >
        <v-list-item class="my-3 d-flex justify-center align-center">
            <v-avatar>
              <v-img 
                  src="../assets/logo.png"
                  alt="logo"

              >
              </v-img>
          </v-avatar>
        </v-list-item>

        <v-divider></v-divider>

        <v-list dense>
            <v-list-item 
                link
                class="mb-3 text-center"
                href="#skills"
            >

              <v-list-item-content>
                  <v-list-item-title>Skills</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-list-item
                link
                class="mb-3 text-center"
                href="#about"
            >

              <v-list-item-content>
                  <v-list-item-title>About</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-list-item
                link
                class="mb-3 text-center"
                href="#contact"
            >

            <v-list-item-content>
                <v-list-item-title>Contact</v-list-item-title>
            </v-list-item-content>
            </v-list-item>

            <v-list-item-icon class="d-flex justify-center align-center">
              <v-btn href="https://www.linkedin.com/in/sharon-rueda-fern%C3%A1ndez-64b2201a7" target="_blank" icon>
                <v-icon>mdi-linkedin</v-icon>
              </v-btn>
              <v-btn href="https://www.instagram.com/sharfe25/" target="_blank" icon class="mr-2">
                <v-icon>mdi-instagram</v-icon>
              </v-btn>
            </v-list-item-icon>

        </v-list>
    </v-navigation-drawer>
</div>
</template>

<script>

export default {
  name: 'AppBar',

  data: () => ({
    mobileMenu:false
  }),
  computed: {
        height () {
            switch (this.$vuetify.breakpoint.name) {
            case 'xs': return true
            case 'sm': return true
            case 'md': return false
            case 'lg': return false
            case 'xl': return false
            }
        },
  }
};
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@300;600&display=swap');
*{
    font-family: 'Raleway', sans-serif !important;
    font-weight: 700 !important;
}
.background_mobile_menu{
  background-color: #d3d3d3d3 !important;
}
</style>