<template>
  <v-footer dark padless>
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
      width="100%"
      style="background-color: #1976d2 !important; border-color: #1976d2 !important"
    >
      <br />
      <v-card-text class="white--text pt-0">
        Мои благодарности, было очень интересно😁<br />
        Старался как мог, но так и не придумал как их идеально отцентрировать. <br />
        Подскажите пожалуйста как это сделать?😥
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>
