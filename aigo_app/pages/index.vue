<template>
  <div>
    <v-carousel
      cycle
      height="400"
      hide-delimiters
      show-arrows-on-hover
    >
      <v-carousel-item
        v-for="(slide, i) in slides"
        :key="i"
      >
        <v-sheet
          :color="colors[i]"
          height="100%"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <div class="display-3">
              {{ slide }}
            </div>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    <br>
    <v-row>
      <v-card
      class="mx-auto"
      max-width="344"
      v-for="(title, i) in titles"
        :key="i"
      >
      <v-img
        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        height="200px"
      ></v-img>

      <v-card-title>
        {{ title }}
      </v-card-title>

      <v-card-subtitle>
        1,000 miles of wonder
      </v-card-subtitle>

      <v-card-actions>
        <v-btn
          color="orange lighten-2"
          text
        >
          Explore
        </v-btn>

        <v-spacer></v-spacer>

        <v-btn
          icon
          @click="show = !show"
        >
          <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
        </v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="show">
          <v-divider></v-divider>

          <v-card-text>
            I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
          </v-card-text>
        </div>
      </v-expand-transition>
    </v-card>
  </v-row>
  <br>
  <br>
  <v-row
    align="center"
    justify="space-around"
  >
    <v-btn
      rounded
      color="success"
      to="/edit" nuxt
    >
      <v-icon left>
        mdi-pencil
      </v-icon>
      記事を執筆
    </v-btn>
  </v-row>
  <br>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
          'deep-purple accent-4',
        ],
        slides: [
          '注目記事1',
          '注目記事2',
          '注目記事3',
          '注目記事4',
          '注目記事5',
        ],
        titles: [
          'dockerについて',
          'GCPの使い方',
          'AIモデルの作り方',
        ],
      }
    },
  }
</script>