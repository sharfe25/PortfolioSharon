<template>
    <v-footer
      class="pa-0"
      color="rgb(115, 56, 226)"
    >
      <v-card
        flat
        tile
        color="rgb(115, 56, 226)"
        width="100%"
        class="text-center"
      >
        <v-card-text class="ma-0 pa-1">
          <v-btn
            class="mx-4"
            dark
            icon
            href="https://www.facebook.com/sharon.ruedafernandez" target="_blank"
          >
            <v-icon size="24px">
              mdi-facebook
            </v-icon>
          </v-btn>
          <v-btn
            class="mx-4"
            dark
            icon
            href="https://www.linkedin.com/in/sharon-rueda-fern%C3%A1ndez-64b2201a7" target="_blank"
          >
            <v-icon size="24px">
              mdi-linkedin
            </v-icon>
          </v-btn>
          <v-btn
            class="mx-4"
            dark
            icon
            href="https://www.instagram.com/sharfe25/" target="_blank"
          >
            <v-icon size="24px">
              mdi-instagram
            </v-icon>
          </v-btn>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <strong>Sharon Rueda</strong>
        </v-card-text>
      </v-card>
    </v-footer>
</template>

<script>

export default {
  name: 'Footer',

  data: () => ({

  }),
};
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@300;600&display=swap');
*{
    font-family: 'Raleway', sans-serif !important;
}
</style>