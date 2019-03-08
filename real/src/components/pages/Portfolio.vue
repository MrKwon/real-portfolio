<template>
  <v-container>
    <v-layout>
      <v-flex xs6 sm6 ma-4>
        <v-card>
          <v-img
            src="https://raw.githubusercontent.com/MrKwon/unitni/master/img/logo/icon_png.png"
            aspect-ratio="2.75"
          ></v-img>

          <v-card-title class="card_text" primary-title>
            <div>
              <h3 class="headline mb-0">Kangaroo Valley Safari</h3>
              <div> {{ card_text }} </div>
            </div>
          </v-card-title>

          <v-card-actions>
            <v-btn flat color="orange">Share</v-btn>
            <v-btn flat color="orange">Explore</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>

      <v-flex xs6 sm6 ma-4>
        <v-card>
          <v-img
            src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
            aspect-ratio="2.75"
          ></v-img>

          <v-card-title class="card_text" primary-title>
            <div>
              <h3 class="headline mb-0">Kangaroo Valley Safari</h3>
              <div> {{ card_text }} </div>
            </div>
          </v-card-title>

          <v-card-actions>
            <v-btn flat color="orange">Share</v-btn>
            <v-btn flat color="orange">Explore</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      card_info: [
        {
          card_img_url: 'https://raw.githubusercontent.com/MrKwon/unitni/master/img/logo/icon_png.png',
          card_title: 'UNITNI 프로토타입',
          card_text: `CEOS 8기 동아리원으로 구성된 프로젝트의 프로토타입입니다.
          프론트와 백 모두 JavaScript를 사용합니다.
          프론트엔드는 Vue.js 프레임워크를 이용하고, 
          백엔드는 Node.js 플렛폼을 이용하였습니다.`
        },
        {
          card_img_url: ''
        }
      ],
      card_text: 'Lorem ipsum dolor sit amet, brute iriure accusata ne mea. Eos suavitate referrentur ad, te duo agam libris qualisque, utroque quaestio accommodare no qui. Et percipit laboramus usu, no invidunt verterem nominati mel. Dolorem ancillae an mei, ut putant invenire splendide mel, ea nec propriae adipisci. Ignota salutandi accusamus in sed, et per malis fuisset, qui id ludus appareat.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  text-align: left;
}
.card_text {
  text-align: left;
}
</style>