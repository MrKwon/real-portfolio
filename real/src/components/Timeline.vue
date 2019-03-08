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
          year: '2018.12 ~ 현재',
          title: '프로젝트 팀 UNITNI 개발자',
          desc: '바쁜 대학생들을 위해 학사정보와 학사일정을 개인 맞춤형으로 제공해주는 웹, 앱 서비스입니다. 현재 팀원들과 함께 지속적으로 디벨롭을 진행 중 입니다.'
        },
        {
          color: 'green',
          year: '2018.09 ~ 현재',
          title: '신촌 연합 IT 창업 동아리 개발자',
          desc: '신촌 연합 IT 창업 동아리 CEOS 에서 개발자 포지션으로 활동하고 있습니다. 현재는 9기 운영진으로 활동하고 있습니다.'
        },
        {
          color: 'pink',
          year: '2018.10 ~ 2019.01',
          title: 'Hong-Ik Start Up 지원 사업 참가',
          desc: 'PalmPay 로 지원 사업에 선정되어 기초 교육 이수와 지원을 받음'
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
</style>