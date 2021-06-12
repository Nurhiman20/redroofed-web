<template>
  <div>
    <div class="py-12">
      <v-row justify="center" align="center">
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <div>
            <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. In non, explicabo voluptate.</h1>
            <p class="mt-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci, laboriosam accusantium dolores culpa reiciendis.</p>
            <v-btn color="primary">Hubungi Kami</v-btn>
          </div>
        </v-col>
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <div class="hidden-sm-and-down">
            <v-img
              contain
              :src="require('@/assets/img/illustration1.png')"
            ></v-img>
          </div>
        </v-col>
      </v-row>
    </div>

    <div class="py-12">
      <v-row justify="center" align="center">
        <v-col cols="12" sm="6" md="6" lg="6" xl="6">
          <div>
            <h1>Penawaran Kami</h1>
            <p class="mt-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci, laboriosam accusantium dolores culpa reiciendis.</p>
          </div>
        </v-col>
        <v-col cols="12" sm="6" md="6" lg="6" xl="6"></v-col>
        <v-col cols="12" sm="4" md="4" lg="4" xl="4" class="mt-n3">
          <v-card min-height="250" class="d-flex flex-column justify-center">
            <div class="pa-4">
              <v-img
                contain
                max-height="100"
                :src="require('@/assets/img/icon1.png')"
              ></v-img>
            </div>
            <v-card-title class="mt-n3 mx-auto">Duis aute irure dolor</v-card-title>
            <v-card-text class="mt-n3 mx-auto text-center">
              Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4" md="4" lg="4" xl="4" class="mt-n3">
          <v-card min-height="250" class="d-flex flex-column justify-center">
            <div class="pa-4">
              <v-img
                contain
                max-height="100"
                :src="require('@/assets/img/icon2.png')"
              ></v-img>
            </div>
            <v-card-title class="mt-n3 mx-auto">Duis aute irure dolor</v-card-title>
            <v-card-text class="mt-n3 mx-auto text-center">
              Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet.
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4" md="4" lg="4" xl="4" class="mt-n3">
          <v-card min-height="250" class="d-flex flex-column justify-center">
            <div class="pa-4">
              <v-img
                contain
                max-height="100"
                :src="require('@/assets/img/icon3.png')"
              ></v-img>
            </div>
            <v-card-title class="mt-n3 mx-auto">Duis aute irure dolor</v-card-title>
            <v-card-text class="mt-n3 mx-auto text-center">
              Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>  
    </div>
  </div>
</template>

<script>
export default {
}
</script>
