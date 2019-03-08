<template>
  <v-layout xs6 mt-2 mb-2 ml-2 mr-4>
    <v-timeline class="timeline">
      <v-timeline-item
        v-for="(year, i) in years"
        :key="i"
        :color="year.color"
        small
      >
        <template v-slot:opposite>
          <span
            :class="`headline font-weight-bold ${year.color}--text`"
            v-text="year.year"
          ></span>
        </template>
        <v-card class="elevation-2">
        
          <v-card-title :class="`headline font-weight-light ${year.color}--text`">{{ year.title }}</v-card-title>
          <v-card-text>
            {{ year.desc }}
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-layout>
</template>

<script>

export default {
  data () {
    return {
      years: [
        {
          color: 'cyan',
          year: '2018.12 ~',
          title: '프로젝트 팀 UNITNI 개발자',
          desc: '바쁜 대학생들을 위해 학사정보와 학사일정을 개인 맞춤형으로 제공해주는 웹, 앱 서비스입니다. 현재 팀원들과 함께 지속적으로 디벨롭을 진행 중 입니다.'
        },
        {
          color: 'green',
          year: '2018.09 ~',
          title: '신촌 연합 IT 창업 동아리 개발자',
          desc: '신촌 연합 IT 창업 동아리 CEOS 에서 개발자 포지션으로 활동하고 있습니다. 현재는 9기 운영진으로 활동하고 있습니다.'
        },
        {
          color: 'pink',
          year: '2018.10 ~ 2019.01',
          title: 'Hong-Ik Start Up 지원 사업 참가',
          desc: 'PalmPay 로 지원 사업에 선정되어 기초 교육 이수와 지원을 받았습니다.'
        },
        {
          color: 'blue',
          year: '2017.09 ~',
          title: '홍익대학교 컴퓨터공학 복수전공',
          desc: '컴퓨터공학 복수전공을 수강하기 시작하였습니다. 자료구조, 알고리즘, 컴퓨터구조, 운영체제 등 다양한 과목을 수강하였습니다.'
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.theme--light.v-timeline:before {
  background: white !important;
}

.v-card__text {
    padding: 16px;
    width: 100%;
    text-align: left;
}
.font-weight-light {
  font-weight: 400 !important;
}



.headline {
  font-size: 18px !important;
  font-weight: 400;
  line-height: 24px !important;
  letter-spacing: normal !important;
  font-family: 'Roboto', sans-serif !important;
}
</style>