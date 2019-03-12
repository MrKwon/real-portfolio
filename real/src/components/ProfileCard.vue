<template>
  <v-container>
    <div class="container">
      <div id="resume-container" class="clearfix">
        <!-- start of resume-->
        <header class="header">
          <v-layout class="resume-layout" column pa-2>
            <v-layout class="resume-inner-layout" row pa-2 mb-2>
              <v-flex xs4>
                <img class="resume-portfolio-pic" src="@/assets/photo/me.jpg">
              </v-flex>
              <v-flex xs8>
                <div class="resume-name">
                  <h1>{{ resume.ko.name }}</h1>
                  <span>{{ resume.ko.role }}</span>
                </div>
              </v-flex>
            </v-layout>
            <v-layout class="resume-inner-layout" row pa-2 mt-2 mb-2>
              <v-flex xs4>
                <div class="resume-info">
                  <address>
                    <i class="fa fa-map-marker">{{ resume.ko.location }}</i>
                  </address>
                </div>
              </v-flex>
              <v-flex xs4>
                <div class="resume-info">
                  <i class="fa fa-paper-plane" />
                  <a href="mailto:[email]?subject=Mail from Jason Kwon Resume">{{ resume.static.email }}</a>
                </div>
              </v-flex>
              <v-flex xs4>
                <div class="resume-info">
                  <i class="fa fa-phone">  </i>
                  <a href="tel:010-3883-9801">{{ resume.ko.phone }}</a>
                </div>
              </v-flex>
            </v-layout>
          </v-layout>
        </header>

        <section id="summary">
          <v-layout row>
            <v-flex xs4 pa-2>
              <div class="col-md-4 summary-box">
                <h2>Summary</h2>
                <p
                  v-for="(sum, i) in resume.ko.summary"
                  :key="i">
                  {{ sum }}
                </p>
              </div>
            </v-flex>
            <v-flex xs4 pa-2>
              <h2>Skills</h2>
                <v-layout column>
                  <v-layout row
                    v-for="(skill, i) in resume.ko.skills"
                    :key="i">
                    <v-flex xs5>
                      <p class="skill-name">{{ skill.name }}</p>
                    </v-flex>
                    <v-flex xs7>
                      <v-progress-linear
                        class="progress-bar"
                        color="info"
                        height="20"
                        :value="skill.stats"
                      >
                        <p class="skill-stats">{{ skill.stats }}</p>
                      </v-progress-linear>
                    </v-flex>
                  </v-layout>
                </v-layout>
            </v-flex>
            <v-flex xs4 pa-2>
              <div class="col-md-4 specializations">
                <h2>Specializations</h2>
                <ul>
                  <li>영문 레퍼런스를 자유롭게 이용할 수 있습니다.</li>
                  <li>Windows, Linux, Mac 세 운영체제 모두에서 개발 경험이 있습니다.</li>
                  <li>기본적인 Git 기능들을 알고 사용이 가능합니다.</li>
                  <li>데이터베이스는 SQL, NoSQL 모두 기본적인 지식들을 습득하고 있습니다.</li>
                  <li>웹 프론트엔드 프레임워크 Vue의 기본적인 내용을 습득하고 자유로운 사용이 가능합니다.</li>
                  <li>안드로이드 스튜디오에서 Java와 Kotlin을 이용한 어플리케이션 개발 경험이 있습니다.</li>
                  <li>AWS EC2 Instance 에 Apache, PHP, MySQL와 Node.js로 웹서버를 구현하여 알파테스트를 진행한 경험이 있습니다.</li>
                  <li>기본적 객체 지향 설계 패턴과 소프트웨어 아키텍쳐를 이해하고 있습니다.</li>
                </ul>
              </div>
            </v-flex>
          </v-layout>
        </section>
      </div><!-- end resume -->
    </div>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      resume: {
        static: {
          email: "erased11@gmail.com",
        },
        ko: {
          name: "권민철",
          role: "소프트웨어 엔지니어",
          location: "서울시",
          phone: "010-3883-9801",
          summary: [
            "홍익대학교에 재학 중이고 경영학과 컴퓨터공학을 전공하고 있는 학생입니다.",
            "웹과 앱 프로그래밍을 공부하고 있으며 프론트엔드와 백엔드 구분 없이 필요하다고 생각한 기술은 공부하고 습득을 위한 프로젝트를 진행하고 있습니다.",
            "IT 창업 동아리 활동을 통해 다양한 분야의 동료들과 협업을 하며 개발 분야 뿐만 아니라 기획, 디자인 분야에 대해서도 이해도가 있습니다.",
            "새로운 기술을 습득하는 것에 대해 매우 개방적이며 자기주도적으로 프로그래밍에 대한 지식을 습득하는 것이 장점입니다."
          ],
          skills: [
            { name: "C/C++", stats: "30%" },
            { name: "Java", stats: "70%" },
            { name: "Kotlin", stats: "50%" },
            { name: "JavaScript", stats: "60%" },
            { name: "Html/CSS", stats: "40%" },
          ]
        }
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url(https://fonts.googleapis.com/css?family=Roboto:400,300);

html, body { background: #777; padding: 20px 0; }	
h5 { font-weight: bold; }

.resume-info {
  color: white;
}

.skill-text {
  padding: 0px;
}

#resume-container {  
  background: rgba(255,255,255,1); 
  color: #2B343A !important;
  opacity: 1 !important; 
  margin-bottom: 40px; 
  padding-bottom: 20px;  
  border-radius: 7px;
  font-family: 'Roboto', sans-serif; 
}

#resume-container a { color: white; text-decoration: underline; font-family: 'Roboto', sans-serif; }

#resume-container hr { border-bottom: 2px solid black; }

#resume-container header { 
  background: #2B343A; 
  padding: 20px 0 0px; 
  position: relative;
  z-index: 1;
  border-top-left-radius: 7px; 
  border-top-right-radius: 7px; 
}


#resume-container header:after {
  background: inherit;
  content: '';
  display: block;
  height: 30%;
  left: 0;
  position: absolute;
  right: 0;
  z-index: -1;
  -webkit-backface-visibility: hidden;
}


#resume-container header:after {
  bottom: 0;
  -webkit-transform: skewY(-2.5deg);
      transform: skewY(-2.5deg);
  -webkit-transform-origin: 100%;
      transform-origin: 100%;
}

#resume-container header .resume-portfolio-pic {
  border-radius: 50%;
  width: 200px;
  height: 200px;
  margin: 0 auto;
  display: block;
  }

.resume-name { text-align: center; color: white; padding-top: 50px; font-family: 'Roboto', sans-serif;  }

#resume-container .contact-info { text-align: center; padding: 10px 0; margin: 20px 0; color: white; font-family: 'Roboto', sans-serif; }
#resume-container .contact-info a  { color: white; font-family: 'Roboto', sans-serif; }


#resume-container #summary { padding: 50px 10px 0; }
#resume-container #summary .summary { padding: 0 20px; }
#resume-container #summary p { text-align: left; }
#resume-container #summary li { text-align: left; }
#resume-container #summary h2 {
  padding-bottom: 12px;
  font-family: 'Roboto', sans-serif;
}
#resume-container #summary .skill-name { text-align: center !important; }
#resume-container #summary .skill-stats { text-align: center !important; }
#resume-container #summary .progress-bar { border-radius: 4px; }

#resume-container .skill-text { text-align: center; }

#resume-container .contact-info .email, #resume-container .contact-info .phone { margin-bottom: 20px; }


#experience { padding: 0 20px; }

#experience h2, #experience h3, #experience h4 { margin: 0 !important; }

#experience .past-employer { padding: 20px 0; }
#experience .employer-img { display: block; margin: 0 auto; padding-top: 20px; }
#experience .short-description { /* padding-top: 20px; */ }


#education { padding: 0 20px; }

#education .past-school { padding: 20px 0; }

#education .past-school .left { text-align: center; }

#computers { padding: 0 20px; }


#resume-container .pills { padding-left: 0; }
#resume-container .pills a { color: black; }
#resume-container .pills li { 
  box-shadow: 0px 1px 1px #CCC;
  transition: all 0.07s ease 0s;
  display: inline-block;
  border: 0px none;
  margin: 0px 5px 5px 0px;
  padding: 0px;
  font-size: 13px;
  line-height: 17px;
  color: black;
  font-weight: normal;
  background: #F1F1F1 none repeat scroll 0% 0%;
  border-radius: 2px;
  text-decoration: none;
}
#resume-container .pills li .wrap {
  display: inline-block;
  padding: 5px 10px 4px;
}

#references { padding: 0 20px; margin: 20px 0; text-align: center; }
#resume-container .linkedin-link { margin-bottom: 10px; }
#resume-container .linkedin-link span { display: block; color: black; text-align: center; }
  
/*~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~MEDIA QUERIES~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~*/
@media only screen and ( min-width: 1100px ) and ( max-width: 1405px) {
  
}

@media only screen and ( min-width: 992px ) {
  #experience .col-md-7 { border-left: 2px solid black; }
  #education .col-md-8 { border-left: 2px solid black; }
}


@media only screen and (max-width: 1200px) {
  
}


@media only screen and (max-width: 990px) {

  .past-employer { border-bottom: 1px solid #dedede; margin-bottom: 20px; }
  .past-employer:last-child { border-bottom: none; margin-bottom: 0; }
  
  .past-school { border-bottom: 1px solid #dedede; }
  .past-school:last-child { border-bottom: none !important; }
  
  #references .col-md-4 { margin-bottom: 20px; }
  
  #experience .employer-img { padding-top: 0; max-width: 200px; }
  
  
}

@media only screen and (max-width: 960px) {
  
}

@media only screen and ( max-width: 768px ) {
  
}
  
@media only screen and (max-width: 665px) {
  .specializations ul { padding-left: 0; }
  .skill-text { margin-bottom: 0; }
}
  
@media only screen and (max-width: 567px) {
  #computers ul { padding-left: 10px; }
}

@media only screen and (max-width: 420px) {
  #extra-skills { display: none; }
}
</style>