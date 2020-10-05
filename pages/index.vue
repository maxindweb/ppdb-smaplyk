<template>
  <v-main>
    <v-carousel
    height="auto"
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
          <h1>Jalur Pendaftaran</h1>
        </v-col>
      </v-row>
      <v-row>
        <v-col 
        v-for="(registration, i) in registrations"
        :key="i"
        >
        <v-skeleton-loader
        type="card-heading, card-avatar"
        loading
        v-if="!loading"
        ></v-skeleton-loader>
          <v-card
          :elevation="5"
          class="rounded-xl"
          v-else
          >
            <v-card-title>
              {{registration.title}}
            </v-card-title>
            <v-card-text>
              {{registration.text}}
            </v-card-text>
          </v-card>
        </v-col>
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
      ],
      registrations: [
        {
          title: 'Jalur Prestasi',
          icon: 'mdi-phone',
          text: 'Jalur prestasi adalah jalur pendaftaran calon peserta didik baru dengan persyaratan berkas seperti jalur reguler, dan ditambah persyaratan nilai mapel UN di rapor minimal 85, ditambah data prestasi kejuaraan dengan perolehan peringkat 1-3 bidang akademik atau olah raga minimal tingkat regional. Jalur ini diperuntukkan bagi calon siswa baru yang berasal dari sekolah lanjutan pertama di dalam atau luar wilayah Daerah Istimewa Yogyakarta'
        },
        {
          title: 'Jalur Khusus',
          text:'Jalur ini diperuntukkan bagi calon peserta didik baru yang berasal dari sekolah menengah pertama di luar wilayah Daerah Istimewa Yogyakarta. Calon peserta didik baru yang melalui jalur khusus tidak melalui proses tes tertulis dan wawancara'
        },
        {
          title: 'Jalur Kerjasama',
          text: 'Jalur bagi para calon peserta didik dari SMP Pangudi Luhur Yogyakarta'
        },
        {
          title: 'Jalur Reguler',
          text: 'Jalur reguler adalah jalur pendaftaran calon peserta didik baru dengan persyaratan kelengkapan berkas, menjalani tes tertulis dan wawancara. Jalur ini diperuntukkan bagi calon peserta didik baru yang berasal dari sekolah lanjutan pertama dalam wilayah Daerah Istimewa Yogyakarta.'
        }
      ],
      loading: true
    }
  }
}
</script>