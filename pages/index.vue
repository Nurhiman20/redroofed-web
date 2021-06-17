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

    <section id="testimoni" class="py-12">
      <v-row justify="center" align="center">
        <v-col cols="12">
          <div>
            <h1 class="font-weight-medium text-center">Testimoni</h1>
          </div>
        </v-col>
        <v-col cols="12" md="4" lg="4" xl="4" class="d-flex flex-column">
          <v-avatar size="120" class="mx-auto">
            <img
              src="https://cdn.vuetifyjs.com/images/john.jpg"
              alt="Photo"
            >
          </v-avatar>
          <h3 class="font-weight-bold text-center mt-3">Ali Baba</h3>
          <p class="text-center grey--text">Siswa Kelas 11</p>
          <p class="text-center font-italic">"Lorem ipsum dolor sit amet consectetur, adipisicing elit. Numquam, reprehenderit nesciunt odit quo dolorum cupiditate accusantium obcaecati eligendi laboriosam dolores?"</p>
        </v-col>
        <v-col cols="12" md="4" lg="4" xl="4" class="d-flex flex-column">
          <v-avatar size="120" class="mx-auto">
            <img
              src="https://cdn.vuetifyjs.com/images/john.jpg"
              alt="Photo"
            >
          </v-avatar>
          <h3 class="font-weight-bold text-center mt-3">Ali Baba</h3>
          <p class="text-center grey--text">Siswa Kelas 11</p>
          <p class="text-center font-italic">"Lorem ipsum dolor sit amet consectetur, adipisicing elit. Numquam, reprehenderit nesciunt odit quo dolorum cupiditate accusantium obcaecati eligendi laboriosam dolores?"</p>
        </v-col>
      </v-row>
    </section>

    <section id="galeri" class="py-12 mt-2">
      <v-row justify="center" align="center">
        <v-col cols="12">
          <div>
            <h1 class="font-weight-medium text-center">Galeri Kelas</h1>
          </div>
        </v-col>        
        <v-col cols="12" class="hidden-md-and-up">
          <v-carousel height="300" hide-delimiters hide-delimiter-background>
            <v-carousel-item
              v-for="(item,i) in imageGallery"
              :key="i"
              :src="item"
              reverse-transition="fade-transition"
              transition="fade-transition"
            ></v-carousel-item>
          </v-carousel>
        </v-col>
        <v-col cols="12" md="4" lg="4" xl="4" v-for="n in imageGallery" :key="n" class="hidden-sm-and-down">          
          <v-img
            max-height="300"
            :aspect-ratio="3/4"
            :src="n"
            class="grey"
          >
            <template v-slot:placeholder>
              <v-row
                class="fill-height ma-0"
                align="center"
                justify="center"
              >
                <v-progress-circular
                  indeterminate
                  color="grey lighten-5"
                ></v-progress-circular>
              </v-row>
            </template>
          </v-img>
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

    <section id="address" class="py-12">
      <v-row justify="center" align="center">
        <v-col cols="12" md="5" lg="5" xl="5">
          <v-img
            contain
            max-height="100"
            :src="require('@/assets/img/logo.png')"
          ></v-img>
          <p class="text-center mt-2">Jl. Villa Bogor Blok G. 1 No.17, RT.05/RW.12, Ciparigi, Kec. Bogor Utara, Kota Bogor, Jawa Barat 16710</p>
          <div class="text-center">
            <v-btn color="primary" small outlined @click="openMap">
              Lihat di Google Maps
            </v-btn>
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
      ],
      imageGallery: ['https://picsum.photos/400/300', 'https://picsum.photos/400/301', 'https://picsum.photos/400/302', 'https://picsum.photos/400/303', 'https://picsum.photos/400/304', 'https://picsum.photos/400/305', 'https://picsum.photos/400/306', 'https://picsum.photos/400/307', 'https://picsum.photos/400/308']
    }
  },
  methods: {
    openMap() {
      window.open('https://maps.app.goo.gl/CAv7m76r7CUT9Pnz8', '_blank').focus();
    }
  },
}
</script>
