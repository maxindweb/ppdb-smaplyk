<template>
  <v-main>
    <v-carousel
    height="auto"
    cycle="true"
    >
      <v-carousel-item
      v-for="(item,i) in items"
      interval="5"
      :key="i"
      :src="item.src"
      :alt="item.alt"
      ></v-carousel-item>
    </v-carousel>
    <v-container>
      <v-row>
        <v-col>
          <h1><span>Jalur Pendaftaraan</span></h1>
        </v-col>
      </v-row>
      <v-row>
        <v-card>
          <v-card-title>
            
          </v-card-title>
        </v-card>
      </v-row>
    </v-container>
  </v-main>
</template>
<script>
export default {
  data () {
    return {
      items: [
        // {
        //   src: 'http://ppdb.smaplyk.sch.id/asset/img/slide/home03.jpg'
        // },
        {
          src: 'carousel1.jpg',
          alt: 'Gelar Budaya SMA Pangudi Luhur Yogyakarta'
        },
        {
          src: 'carousel2.jpg',
          alt: 'Gelar Budaya SMA Pangudi Luhur Yogyakarta'
        },
        {
          src: 'dbl1.jpg'
        }
      ]
    }
  }
}
</script>