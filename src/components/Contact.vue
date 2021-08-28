<template>
<v-card
    id="contact"
    tile
    color="#1D1D1D"
    elevation="0" 
    class="d-flex justify-center cardSkills d-flex skillsText"
>
    <v-card tile elevation="0"  class="pt-6 text-center px-5" shaped rounded>
        <v-card-text class="titleSkills pt-5 pl-5 text-center">
            Contact Me
        </v-card-text>
        <v-row
        class="pt-6 px-3"
        >
            <v-form 
              ref="support_form"       
              >
              <v-row no-gutters justify="space-around">
                <v-col cols="6" class="px-3">
                  <v-text-field
                      v-model="name"
                      label="Name"
                      required
                  ></v-text-field>
                </v-col>
                <v-col cols="6" class="px-3">
                  <v-text-field
                      v-model="email"
                      label="Email"
                      required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" class="px-3">
                  <v-text-field
                      v-model="subject"
                      label="Subject"
                      required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" class="px-3">
                  <v-textarea
                      v-model="message"
                      label="Message"
                      required
                  ></v-textarea>
                </v-col>
              </v-row>
              
            </v-form>
        </v-row>
        <v-btn
            color="rgb(70, 159, 241)"
            outlined
            @click="sendMessage"
            class="mb-4 mt-2"
        >
            Send Message
        </v-btn>
    </v-card>
</v-card>
</template>

<script>
  export default {
    name: 'Contact',

    components: {
      
    },
    data () {
        return{
            name:'',
            email:'',
            subject:'',
            message:''
        }
    },
    methods:{
        sendMessage(){
            this.name=''
            this.email=''
            this.subject=''
            this.message=''
        }
    }
  }
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@300;600&display=swap');
.skillsText{
    font-family: 'Raleway', sans-serif !important; 
}
.titleSkills{
    font-weight:700 !important;
    font-size: calc(2em + 2vw) !important;
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