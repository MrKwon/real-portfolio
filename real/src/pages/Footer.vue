<template>
  <div class="section fp-auto-height">
    <template>
      <v-footer
        dark
        height="200px"
      >
        <v-card
          flat
          tile
          class="black white--text text-xs-center"
          height="200px"
          width="100%"
        >
          <v-card-text>
            <v-btn
              v-for="(item, i) in items"
              :key="i"
              class="mx-3 white--text"
              icon
              :href="item.url"
            >
              <v-icon size="24px" >{{ item.icon }}</v-icon>
            </v-btn>
          </v-card-text>

          <v-card-text class="white--text pt-0">
            This Website is implemented by Jason Kwon using Vue, Vuetify, Fullpage and Animation Resources are referenced from codepen.io.
            Bouncing profile card by <a herf="http://balap.us/">Bhakti Al Akbar</a>. 
          </v-card-text>

          <v-divider></v-divider>

          <v-card-text class="white--text">
            &copy;2019 — <strong>Jason Kwon</strong>
          </v-card-text>
        </v-card>
      </v-footer>
    </template>
  </div>  
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        icon: 'fab fa-facebook',
        url: 'https://facebook.com/kwon140'
      },
      {
        icon: 'fab fa-instagram',
        url: 'http://instagram.com/kwonmc_'
      },
      {
        icon: 'fab fa-linkedin',
        url: 'https://www.linkedin.com/in/kwon140/'
      },
      {
        icon: 'fab fa-github',
        url: 'https://github.com/mrkwon'
      }
    ]
  })
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  height: 200px !important;
}
.section {
  background: black;
  height: 200px !important;
  width: 100%;
}

div {
  color: white;
}


</style>