<template>
  <v-container>
    <section id="cd-timeline" class="cd-container">
      <div
        class="cd-timeline-block"
        v-for="(content, i) in contents"
        :key="i">
        <div class="cd-timeline-img cd-movie">
        </div>
        <div class="cd-timeline-content">
          <h2>{{ content.ko.title }}</h2>
          <div class="timeline-content-info">
            <span class="timeline-content-info-title">
              <i class="fa fa-certificate" aria-hidden="true"></i>
                {{ content.ko.role }}
            </span>
            <span class="timeline-content-info-date">
              <i class="fa fa-calendar-o" aria-hidden="true"></i>
              {{ content.ko.term }}
            </span>
          </div>
          <p>{{ content.ko.brief }}</p>
          <ul class="content-skills">
            <li v-for="(skill, j) in content.ko.skills" :key="j">{{ skill.name }}</li>
          </ul>
        </div>
      </div>
    </section>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      options: {
        scrollOverflow: true,
        scrollOverflowReset: false,
      },
      contents: [
        {
          ko: {
            title: "우아한 테크코스",
            role: "크루",
            term: "2019.05 - 현재",
            brief: `배달의 민족을 서비스 하는 우아한 형제들의 웹 백엔드 교육에 합격하여 교육을 받고 있습니다. 우아한 테크코스는 스타트업의 문화와 개발 프로세스를 몸소 체험하며 교육을 받을 수 있는 프로그램 입니다.`,
            skills: [
              { name: "Java" },
              { name: "JUnit" },
            ]
          },
          // en: { }
        },
        {
          ko: {
            title: "팀 프로젝트 UNITNI",
            role: "풀스택 개발자",
            term: "2018.12 - 현재",
            brief: "팀원들의 기획안과 디자이너의 디자인을 취합하여 구현하는 역할을 하고 있습니다. " +
                  "웹과 모바일 어플리케이션, 크로스 플랫폼으로 서비스를 제공하기 위해 Vue로 프론트엔드를 Node로 백엔드를 구현하였습니다. 모바일 어플리케이션은 빌드를 위해 Vue-Native를 이용합니다.",
            skills: [
              { name: "HTML5" },
              { name: "CSS3" },
              { name: "JavaScript" },
              { name: "Vue.js" },
              { name: "Node.js" },
              { name: "MariaDB" },
            ]
          },
          // en: { }
        },
        {
          ko: {
            title: "신촌 연합 IT 창업 동아리 CEOS",
            role: "운영진, 개발자",
            term: "2018.09 - 현재",
            brief: "동아리 내의 개발자 역할을 하며 웹 페이지 유지 보수를 담당하고 있습니다. " +
                  "또한 동아리 운영에 필요한 다양한 역할들을 하고 있습니다.",
            skills: [
              { name: "HTML5" },
              { name: "CSS3" },
              { name: "JavaScript" },
              { name: "Wordpress" },
            ]
          },
          // en: { }
        },
        {
          ko: {
            title: "PalmPay",
            role: "총괄 기획, 운영, 개발",
            term: "2018.06 - 2019.01",
            brief: "\"손바닥 안의 간편한 주문 결제\"를 구현하여 창업을 하기 위해 개발을 진행하였습니다. " +
                    "해당 아이템으로 Hong-Ik Start Up 지원 사업에 선정되어 지원을 받으며 교육을 이수하였습니다. " +
                    "또한 기획, 개발 양면에서 총괄하여 모든 것을 진행하였습니다.",
            skills: [
              { name: "Android" },
              { name: "XML" },
              { name: "Java" },
              { name: "Node.js" },
              { name: "JavaScript" },
              { name: "MariaDB" },
            ]
          },
          // en: { }
        },
        {
          ko: {
            title: "홍익대학교 컴퓨터공학과",
            role: "복수전공",
            term: "시작 : 2017.09",
            brief: "C, C++ 두 가지 언어와 전산학 기초 지식을 습득하고 있습니다. 현재 프로그래밍 언어(4.0/4.5), 알고리즘(3.5/4.5), 운영체제(3.5/4.5), C프로그래밍(4.5/4.5) 및 기타 선수 과목들을 수강하였습니다. "
          },
          // en: { }
        },
        {
          ko: {
            title: "홍익대학교 경영학과",
            role: "주전공",
            term: "시작 : 2013.03",
            brief: "경영학 학사 수준의 지식을 습득하였습니다. 특히 생산, MIS 분야에 대한 깊이 있는 지식을 가지고 있습니다. 또한 김승범 교수의 프로젝트에 연구 보조로 참여한 경험이 있습니다."
          },
          // en: { }
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
html, body {
  // background-color: #708090;//#222C32;
  height: 100%;
  font-family: 'Open Sans', sans-serif;
  box-sizing: border-box;
}

h2 {
  text-align: center;
}

span {
  text-align: center
}
.container {
  -webkit-box-flex: 1;
    -ms-flex: 1 1 100%;
    flex: 1 1 100%;
    margin: auto;
    padding-top: 0;
    padding-bottom: 0;
    padding-right: 24px;
    padding-left: 24px;
    width: 100%;
}
@media only screen and (max-width: 959px) {
  .container {
      padding-top: 0;
      padding-bottom: 0;
      padding-right: 16px;
      padding-left: 16px;
  }
}

.cd-container {
  width: 90%;
  max-width: 1080px;
  margin: 0 auto;
  // background: #708090; //#2B343A;
  padding: 0 10%;
  border-radius: 2px;
}
.cd-container::after {
  content: '';
  display: table;
  clear: both;
}

/* -------------------------------- 

Main components 

-------------------------------- */


#cd-timeline {
  position: relative;
  padding: 2em 0;
  // margin-top: 2em;
  // margin-bottom: 2em;
}
#cd-timeline::before {
  content: '';
  position: absolute;
  top: 0;
  left: 25px;
  height: 100%;
  width: 4px;
  background: #FFFFFF // #7E57C2;
}
@media only screen and (min-width: 1265px) {
  #cd-timeline {
    // margin-top: 3em;
    // margin-bottom: 3em;
  }
  #cd-timeline::before {
    left: 50%;
    margin-left: -2px;
  }
}

.cd-timeline-block {
  position: relative;
  margin: 2em 0;
}
.cd-timeline-block:after {
  content: "";
  display: table;
  clear: both;
}
.cd-timeline-block:first-child {
  margin-top: 0;
}
.cd-timeline-block:last-child {
  margin-bottom: 0;
}
@media only screen and (min-width: 1265px) {
  .cd-timeline-block {
    margin: 0 0;
    // margin: 4em 0;
  }
  .cd-timeline-block:first-child {
    margin-top: 0;
  }
  .cd-timeline-block:last-child {
    margin-bottom: 0;
  }
}

.cd-timeline-img {
  position: absolute;
  top: 8px;
  left: 12px;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  box-shadow: 0 0 0 4px #DFDFDF, inset 0 2px 0 rgba(0, 0, 0, 0.08), 0 3px 0 4px rgba(0, 0, 0, 0.05);
  // #7E57C2
}
.cd-timeline-img {
  background: #FFFFFF //#673AB7;
}
@media only screen and (min-width: 1265px) {
  .cd-timeline-img {
    width: 30px;
    height: 30px;
    left: 50%;
    margin-left: -15px;
    margin-top: 15px;
    /* Force Hardware Acceleration in WebKit */
    -webkit-transform: translateZ(0);
    -webkit-backface-visibility: hidden;
  }
}

.cd-timeline-content {
  position: relative;
  margin-left: 60px;
  margin-right: 30px;
  background: #333C42;
  border-radius: 2px;
  padding: 1em;
  .timeline-content-info {
    background: #2B343A;
    padding: 5px 10px;
    color: rgba(255,255,255,0.7);
    font-size: 12px;
    box-shadow:  inset 0 2px 0 rgba(0, 0, 0, 0.08);
    border-radius: 2px;
    i {
      margin-right: 5px;
    }
    .timeline-content-info-title, .timeline-content-info-date {  
      width: calc(50% - 2px);
      display: inline-block;
    }
    @media (max-width: 500px) {
      .timeline-content-info-title, .timeline-content-info-date {  
        display: block;
        width:100%;
      } 
    }
  }
  .content-skills {
    font-size: 12px;
    padding:0;
    margin-bottom: 0;
    display:flex;
    flex-wrap: wrap;
    justify-content: center;
    li {
      background: #40484D;
      border-radius: 2px;
      display: inline-block;
      padding: 2px 10px;
      color: rgba(255,255,255,0.7);
      margin: 3px 2px;
      text-align: center;
      flex-grow: 1;
    }
  }
}
.cd-timeline-content:after {
  content: "";
  display: table;
  clear: both;
}
.cd-timeline-content h2 {
  color: rgba(255,255,255,.9);
  margin-top:0;
  margin-bottom: 5px;
}
.cd-timeline-content p, .cd-timeline-content .cd-date {
  color: rgba(255,255,255,.7);
  font-size: 13px;
  font-size: 0.8125rem;
}
.cd-timeline-content .cd-date {
  display: inline-block;
}
.cd-timeline-content p {
  margin: 1em 0;
  line-height: 1.6;
  text-align: left;
}

.cd-timeline-content::before {
  content: '';
  position: absolute;
  top: 16px;
  right: 100%;
  height: 0;
  width: 0;
  border: 7px solid transparent;
  border-right: 7px solid #333C42;
}

@media only screen and (min-width: 768px) {
  .cd-timeline-content h2 {
    font-size: 20px;
    font-size: 1.25rem;
  }
  .cd-timeline-content p {
    font-size: 16px;
    font-size: 1rem;
  }
  .cd-timeline-content .cd-read-more, .cd-timeline-content .cd-date {
    font-size: 14px;
    font-size: 0.875rem;
  }
}
@media only screen and (min-width: 1265px) {
  .cd-timeline-content {
    color: white;
    margin-left: 0;
    padding: 1.6em;
    width: 36%;
    margin: 0 5%
  }
  .cd-timeline-content::before {
    top: 24px;
    left: 100%;
    border-color: transparent;
    border-left-color: #333C42;
  }
  .cd-timeline-content .cd-date {
    position: absolute;
    width: 100%;
    left: 122%;
    top: 6px;
    font-size: 16px;
    font-size: 1rem;
  }
  .cd-timeline-block:nth-child(even) .cd-timeline-content {
    float: right;
  }
  .cd-timeline-block:nth-child(even) .cd-timeline-content::before {
    top: 24px;
    left: auto;
    right: 100%;
    border-color: transparent;
    border-right-color: #333C42;
  }
  .cd-timeline-block:nth-child(even) .cd-timeline-content .cd-read-more {
    float: right;
  }
  .cd-timeline-block:nth-child(even) .cd-timeline-content .cd-date {
    left: auto;
    right: 122%;
    text-align: right;
  }
}
</style>