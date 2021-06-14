<template>
  <div>
    <section id="hero" class="py-12 mt-2">
      <v-row justify="center" align="center">
        <v-col cols="12" md="6" lg="6" xl="6">
          <div>
            <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. In non, explicabo voluptate.</h1>
            <p class="mt-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci, laboriosam accusantium dolores culpa reiciendis.</p>
            <v-btn color="primary">Hubungi Kami</v-btn>
          </div>
        </v-col>
        <v-col cols="12" md="6" lg="6" xl="6">
          <div class="hidden-sm-and-down">
            <v-img
              contain
              :src="require('@/assets/img/illustration1.png')"
            ></v-img>
          </div>
        </v-col>
      </v-row>
    </section>

    <section id="penawaran" class="py-12 mt-2">
      <v-row justify="center" align="center">
        <v-col cols="12" md="5" lg="5" xl="5" class="mb-n4">
          <div>
            <h1 class="font-weight-medium text-center">Penawaran Kami</h1>
            <p class="mt-2 text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci, laboriosam accusantium dolores culpa reiciendis.</p>
          </div>
        </v-col>
      </v-row>
      <v-row justify="center" align="center">
        <v-col cols="12" md="3" lg="3" xl="3" class="px-12 px-md-4 px-lg-4 px-lg-4" v-for="(penawaran, index) in listPenawaran" :key="index">
          <v-card min-height="250" class="d-flex flex-column justify-center">
            <div class="pa-4">
              <v-img
                contain
                max-height="100"
                :src="penawaran.image"
              ></v-img>
            </div>
            <v-card-title class="mt-n3 mx-auto">{{ penawaran.title }}</v-card-title>
            <v-card-text class="mt-n3 mx-auto text-center">
              {{ penawaran.description }}
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </section>

    <section id="tentang" class="py-12 mt-2">
      <v-row justify="center" align="center">
        <v-col cols="12" md="6" lg="6" xl="6">
          <div>
            <v-img
              contain
              max-height="350"
              :src="require('@/assets/img/illustration2.png')"
            ></v-img>
          </div>
        </v-col>
        <v-col cols="12" md="6" lg="6" xl="6">
          <div>
            <h1 class="font-weight-medium">Tentang Kami</h1>
            <p class="mt-2">At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident, similique sunt in culpa qui officia deserunt mollitia animi, id est laborum et dolorum fuga. Et harum quidem rerum facilis est et expedita istinctio.</p>
          </div>
        </v-col>        
      </v-row>
    </section>

    <section id="kontak" class="py-12 mt-2 mb-12">
      <v-row justify="center" align="center">
        <v-col cols="12" md="4" lg="4" xl="4" class="d-flex flex-column">
          <h2 class="text-center font-weight-medium">Spesial untuk kamu</h2>
          <p class="text-center">Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat facere.</p>
          <div class="d-flex flex-row justify-center align-center">
            <v-icon color="success" class="my-auto">mdi-whatsapp</v-icon>
            <p class="my-auto ml-2 font-weight-bold">0821-2312-3412</p>
          </div>
          <div class="mx-auto">
            <v-btn color="primary" small class="mt-3">Hubungi sekarang</v-btn>
          </div>
        </v-col>        
      </v-row>
    </section>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Beranda',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci, laboriosam accusantium dolores culpa reiciendis.'
      }
    ],
  },
  data() {
    return {
      listPenawaran: [
        {
          title: 'Duis aute irure dolor',
          description: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet.',
          image: require('@/assets/img/icon1.png')
        },
        {
          title: 'Duis aute irure dolor',
          description: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet.',
          image: require('@/assets/img/icon2.png')
        },
        {
          title: 'Duis aute irure dolor',
          description: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet.',
          image: require('@/assets/img/icon3.png')
        }
      ]
    }
  },
}
</script>
