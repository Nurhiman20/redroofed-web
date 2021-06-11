<template>
  <div>
    <div class="mt-4">
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
  </div>
</template>

<script>
export default {
}
</script>
