<template>
  <section id="about">
    <v-container fluid id="features" class="mt-2">
      <v-row align="center" justify="center">
        <v-col cols="10">
          <h1 class="text-center pt-6 font-weight-light display-2">
            PSB Pesantren
          </h1>
          <v-divider class="my-6"></v-divider>
          <v-row align="center" justify="space-around">
            <!-- <v-col cols="12" class="text-center">
              <h1 class="font-weight-light display-2">Title</h1>
              <h1 class="font-weight-light">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </h1>
            </v-col> -->
            <v-col
              cols="12"
              sm="4"
              class="text-center"
              v-for="(feature, i) in features"
              :key="i"
            >
              <v-hover v-slot:default="{ hover }">
                <v-card
                  class="card"
                  shaped
                  :elevation="hover ? 10 : 4"
                  :class="{ up: hover }"
                >
                  <v-img
                    :src="feature.img"
                    max-width="100px"
                    class="d-block ml-auto mr-auto"
                    :class="{ 'zoom-efect': hover }"
                  ></v-img>
                  <h1 class="font-weight-regular">{{ feature.title }}</h1>
                  <v-chip
                    close-icon="mdi-close-outline"
                    color="primary"
                    link
                    outlined
                  >
                    {{ feature.text }}
                  </v-chip>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-row align="center" justify="center">
        <v-col cols="10">
          <h1 class="text-center pt-6 font-weight-light display-2">
            PPDB Sekolah
          </h1>
          <v-divider class="my-6"></v-divider>
          <v-row align="center" justify="space-around">
            <!-- <v-col cols="12" class="text-center">
              <h1 class="font-weight-light display-2">Title</h1>
              <h1 class="font-weight-light">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </h1>
            </v-col> -->
            <v-col
              cols="12"
              sm="4"
              class="text-center"
              v-for="(skl, i) in sekolah"
              :key="i"
            >
              <v-hover v-slot:default="{ hover }">
                <v-card
                  class="card"
                  shaped
                  :elevation="hover ? 10 : 4"
                  :class="{ up: hover }"
                >
                  <v-img
                    :src="skl.img"
                    max-width="100px"
                    class="d-block ml-auto mr-auto"
                    :class="{ 'zoom-efect': hover }"
                  ></v-img>
                  <h1 class="font-weight-regular">{{ skl.title }}</h1>
                  <v-chip
                    close-icon="mdi-close-outline"
                    color="primary"
                    link
                    outlined
                  >
                    {{ skl.text }}
                  </v-chip>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          img: "/images/icon2.png",
          title: "23",
          text: "Komplek Ibnu Mas'ud",
        },
        {
          img: "/images/icon1.png",
          title: "20",
          text: "Komplek Masjid Jami'",
        },
        {
          img: "/images/icon3.png",
          title: "4",
          text: "Komplek Tahfidzul Qur'an",
        },
        {
          img: "/images/icon3.png",
          title: "4",
          text: "Komplek Darul Ghuroba",
        },
        {
          img: "/images/icon3.png",
          title: "15",
          text: "Komplek An-Nur",
        },
      ],
      sekolah: [
        {
          img: "/images/icon2.png",
          title: "23",
          text: "SMK 1 Al Hikmah 1",
        },
        {
          img: "/images/icon1.png",
          title: "20",
          text: "SMK 2 Al Hikmah 1",
        },
        {
          img: "/images/icon3.png",
          title: "4",
          text: "MA Al Hikmah 1",
        },
        {
          img: "/images/icon3.png",
          title: "4",
          text: "MTs Al Hikmah 1",
        },
        {
          img: "/images/icon3.png",
          title: "15",
          text: "SMP Al Hikmah 1",
        },
        {
          img: "/images/icon3.png",
          title: "15",
          text: "MMA Al Hikmah 1",
        },
      ],
    };
  },
};
</script>

<style scoped>
#about {
  background-color: #f4f7f5;
}
.card {
  min-height: 225px;
  padding: 10px;
  transition: 0.5s ease-out;
}

.card .v-image {
  margin-bottom: 15px;
  transition: 0.75s;
}

.card h1 {
  margin-bottom: 10px;
}

.zoom-efect {
  transform: scale(1.1);
}

.up {
  transform: translateY(-20px);
  transition: 0.5s ease-out;
}
</style>
