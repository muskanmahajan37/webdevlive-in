<template>
<v-container fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" md="5" lg="4" class="text-center">
        <v-img :src="require('@/assets/img/home.png')">
          <template v-slot:placeholder>
            <v-row class="fill-height ma-0" align="center" justify="center">
              <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
            </v-row>
          </template>
        </v-img>
      </v-col>
      <v-col cols="12" md="7" lg="7">
        <h1
          class="google-font mt-5 mb-0"
          :class="this.$vuetify.theme.dark?'white--text':'grey--text text--darken-2'"
        >web.dev LIVE India</h1>
        <p class="google-font mt-0" style="font-size:80%">
          Follow up event of
          <a rel="noreferrer" href="https://web.dev/live/" target="_blank">web.dev</a>
        </p>
        <p
          class="google-font"
          style="font-size:130%"
        >Bringing Indian web developers together, from home</p>
        <p
          class="google-font"
        >These are unprecedented times, with people worldwide looking to stay connected and informed. The Web plays a special role here, and we're proud to see how the community has stepped up.</p>
        <p
          class="google-font"
        >Join Google's Web Platform team, from the comfort of your homes, to celebrate our community's actions, learn modern web techniques and connect with each other.</p>

        <p class="google-font" :class="this.$vuetify.theme.dark?'white--text':'grey--text text--darken-2'" style="font-size:120%">July 9-12, 2020 | 05:00 PM to 08:00 PM IST</p>

        <p class="google-font" style="font-size:100%;color:#9e9e9e">
          <span v-for="(item,i) in mainData.hashtags" :key="i">
            <v-chip
              :href="'https://twitter.com/hashtag/'+item"
              rel="noopener"
              target="_blank"
              small
              label
              class="mr-1"
            >#{{item}}</v-chip>
            <!-- &nbsp; -->
          </span>
        </p>
        <router-link to="/register">
          <v-btn
            aria-label="Home BTN"
            color="primary"
            style="text-transform: capitalize;"
            class="google-font"
            depressed
            large
            dark
          >Register Here</v-btn>
        </router-link>

        <!-- <v-btn
            aria-label="Home BTN"
            color="primary"
            style="text-transform: capitalize;"
            class="google-font"
            depressed
            large
            target="_blank"
            href="http://goo.gle/webdevliveindia"
            dark
        >Register Here 2</v-btn> -->
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  import aboutEvent from "@/assets/data/about.json";
  export default {
    data: ()=>({
      mainData:{}
    }),
    mounted(){
      this.mainData = aboutEvent
    }
  }
</script>