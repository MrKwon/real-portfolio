<template>
  <div class="section">
    <v-container grid-list-xl pa-5>
      <v-layout :column="width" wrap>
        <v-flex d-flex xs6
          v-for="(item, i) in card_info"
          :key="i">
          <v-card class="card">
            <v-img
              :src="item.img_url"
              aspect-ratio="2.75"
            ></v-img>

            <v-card-title class="card_text" primary-title>
              <div>
                <h3 class="headline mb-3">{{ item.title }}</h3>
                <div> {{ item.text }} </div>
              </div>
            </v-card-title>

            <v-card-actions>
              <v-btn flat color="grey" :href="item.git_url">Github</v-btn>
              <v-spacer></v-spacer>
              <v-btn icon @click="item.show = !item.show">
                <v-icon>{{ item.show ? 'keyboard_arrow_up' : 'keyboard_arrow_down' }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-slide-y-transition>
              <v-card-text class="card_content" v-show="item.show">
                <h3>세부사항</h3>
                <div
                  v-for="(stk, j) in item.stack"
                  :key="j">
                  <li> {{ stk.name }} </li>
                </div>
              </v-card-text>
            </v-slide-y-transition>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      width: false, // 아래의 기준 보다 넓을 때
      card_info: [
        {
          show: false,
          img_url: 'https://raw.githubusercontent.com/MrKwon/real-portfolio/master/real/src/assets/logo/UNITNI_1050x400.png',
          title: 'UNITNI Prototype 클라이언트 및 서버',
          text: `CEOS 8기 동아리원으로 구성된 프로젝트의 프로토타입입니다. 기획자 2명, 디자이너 1명과 협업을 진행한 프로젝트 입니다. 프론트와 백 모두 JavaScript를 사용합니다. 프론트엔드는 Vue.js 프레임워크를 이용하고, 백엔드는 Node.js 플렛폼을 이용하였습니다.`,
          stack: [
            { name : "Vue (프론트엔드)" },
            { name : "jwt / axios / vuex / vue-router / webtoken 기반 인증 구현" },
            { name : "Node (백엔드)" },
            { name : "pm2 / express" },
          ],
          git_url: 'https://github.com/MrKwon/unitni'
        },
        {
          show: false,
          img_url: 'https://raw.githubusercontent.com/MrKwon/real-portfolio/master/real/src/assets/logo/palmpay.png',
          title: 'PalmPay 클라이언트 및 서버',
          text: `"손바닥 안의 주문 결제" 라는 슬로건을 가지고 이용자의 부가적인 행동이 필요없는 결제 문화를 만들고 싶어 시작하게 되었습니다. 클라이언트는 Java를 사용하여 안드로이드 네이티브로 구현하였고, 서버는 JavaScript를 사용하여  Node 서버를 구현하였습니다.`,
          stack: [
            { name : "Android (프론트엔드)" },
            { name : "OkHttp3 / Retrofit2 / Beacon / Socket.io 등 이용" },
            { name : "Node (백엔드)" },
            { name : "Socket" },
          ],
          git_url: 'https://github.com/MrKwon/palmapps'
        }
      ],
    }
  },
  created() {
    window.addEventListener('resize', this.handleResize)
    this.handleResize();
  },
  destroyed() {
    window.removeEventListener('resize', this.handleResize)
  },
  methods: {
    handleResize() {
      this.width = window.innerWidth < 750 ? true : false;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url(https://fonts.googleapis.com/css?family=Noto+Sans+KR:400,700&subset=korean);

h3 {
  text-align: left;
}
div {
  font-family: 'Noto Sans KR', sans-serif;
  color: #2E2E2E;
}
li {
  text-align: left;
}
.card_text {
  text-align: left;
  font-family: 'Noto Sans KR', sans-serif !important;
}
.headline {
  font-size: 24px !important;
  font-weight: 700;
  line-height: 32px !important;
  color: black !important;
  letter-spacing: normal !important;
  font-family: 'Noto Sans KR', sans-serif !important;
}

.card_content {
  background: lightgrey;
}

.card {
  border-radius: 5px;
}


@media only screen and (max-width: 550px) {
  .headline {
    font-size: 20px !important;
    font-weight: 700 !important;
    line-height: 24px !important;
    color: black !important;
    letter-spacing: normal !important;
    font-family: 'Noto Sans KR', sans-serif !important;
  }
}


@media only screen and (max-width: 465px) {
  .headline {
    font-size: 16px !important;
    font-weight: 700 !important;
    line-height: 20px !important;
    color: black !important;
    letter-spacing: normal !important;
    font-family: 'Noto Sans KR', sans-serif !important;
  }
}
</style>