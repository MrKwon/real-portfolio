<template>
  <v-container class="outer_layout">
    <div class="title_profile"><span>WHO IS Jason Kwon</span></div>
    <div class="title_desc"><span>Hover the bouncing ball</span></div>
    <aside class="profile-card">
      <header>
        <a>
          <img src="@/assets/photo/me.jpg">
        </a>
        <h1>{{ info.ko.name }}</h1>
        <h2>{{ info.ko.role }}</h2>
      </header>

      <div class="profile-bio">
        <p>
          {{ info.ko.bio }}
        </p>
      </div>
      
      <ul class="profile-social-links">
        <li>
          <a href="https://facebook.com/kwon140">
            <img src="@/assets/logo/sns/facebook.svg">
          </a>
        </li>
        <li>
          <a href="http://instagram.com/kwon_mc">
            <img src="@/assets/logo/sns/instagram.svg">
          </a>
        </li>
        <li>
          <a href="https://linkedin.com/kwon140">
            <img src="@/assets/logo/sns/linkedin.svg">
          </a>
        </li>
        <li>
          <a href="https://github.com/mrkwon">
            <img src="@/assets/logo/sns/github.svg">
          </a>
        </li>
      </ul>
    </aside>
    <div class="copyright"><span>Scroll Down To Continue</span></div>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      facebook: "facebook",
      info: {
        en: {
          name: "Jason Kwon",
          role: "Software Engineer",
          bio: `Jason Kwon is a Software Engineer\n
              who loves study computer programming\n
              using Java, Kotlin, JavaScript etc.`
        },
        ko: {
          name: "권민철",
          role: "소프트웨어 개발자",
          bio: `Java, Kotlin, JavaScript로 앱/웹을 개발하며
          프로그래밍을 사랑하는
          소프트웨어 개발자입니다.`
        }
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
/* go on then, styles go here.. knock yourself out! */

@import url(https://fonts.googleapis.com/css?family=Old+Standard+TT:400,400italic,700);
@import url(https://fonts.googleapis.com/css?family=Roboto:400,300);
@import url(https://fonts.googleapis.com/css?family=Poppins:400);

$old: 'Old Standard TT', serif;
$roboto: 'Roboto', sans-serif;

.outer_layout {
  width: 100%;
  height: 100%;
}

.title_profile {
  position: relative;
  font-size: 3rem;
  font-family: 'Poppins', sans-serif !important;
  font-weight: 400 !important;
  top: 8%;
}

.title_desc {
  position: relative;
  top: 10%;
  text-align: center;
  font-family: "Roboto" !important;
}
.title_desc span {
  line-height: 36px;
  color: rgba(255, 255, 255, 0.75);
  font-weight: 300;
}
aside {
  width: 350px;
  background: transparent;
  margin: 0 auto;
  position: relative;
  top: 40%;
  transform: translate3d(0, -50%, 0);
  overflow: hidden;
  box-shadow: 0px 1px 4px rgba(0,0,0,0);
  
  &:hover {
    box-shadow: 0px 5px 4px rgba(0,0,0,0.3);
    transition: .5s all ease .25s;
  }
  
  &:hover:before {
    top: 50%;
    transform: translate3d(-50%, -50%, 0) scale(1);
    transition: .3s top ease, .5s transform ease .25s;
  }
  
  &:hover:after {
    opacity: 0;
  }
  
  &:hover header a {
    transform: rotateX(0deg) scale(1);
    transition: .3s all ease .5s;
  }
  
  &:hover header:before,
  &:hover header:after {
    transform: translate3d(0, 0%, 0);
    transition: .3s all ease .8s;
  }
  
  &:hover header h1 {
    opacity: 1;
    transition: .3s all ease .95s;
  }
  
  &:hover header h2 {
    opacity: 1;
    transition: .3s all ease 1.1s;
  }
  
  &:hover .profile-bio:before {
    width: 50px;
    transition: .3s all ease 1.25s;
  }
  
  &:hover .profile-bio p {
    opacity: 1;
    transition: .3s all ease 1.4s;
  }
  
  &:hover .profile-social-links li {
    transform: scale(1);
  }
  
  &:hover .profile-social-links li:first-child {
    transition: .3s all ease 1.55s;
  }
  
    &:hover .profile-social-links li:nth-child(2) {
    transition: .3s all ease 1.7s;
  }
  
    &:hover .profile-social-links li:nth-child(3) {
    transition: .3s all ease 1.85s;
  }
  
    &:hover .profile-social-links li:last-child {
    transition: .3s all ease 2.00s;
  }
  
  &:before {
    content: "";
    position: absolute;
    width: 1100px;
    height: 1100px;
    background: white;
    border-radius: 50%;
    top: 90%;
    left: 50%;
    transform: translate3d(-50%, -50%, 0) scale(.025);
    animation: .5s bounce infinite alternate-reverse;
    transition: .5s transform ease;
  }
  
  &:after {
    content: "";
    position: absolute;
    left: 160px;
    right: 160px;
    bottom: 0;
    height: 15px;
    background: rgba(0,0,0,.5);
    border-radius: 50%;
    transition: .3s opacity ease;
    animation: .5s shadow infinite alternate-reverse;
  }
  
  header {
    position: relative;
    display: block;
    
    &:before {
      content: "";
      position: absolute;
      left: 0;
      right: 0;
      height: 200px;
      background: url("http://balapastudio.co/almond/images/demo/balapa.png") no-repeat;
      background-size: cover;
      transform: translate3d(0, -100%, 0);
    }
    
    &:after {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 200px;
      background: rgba(0,0,0,.5);
      transform: translate3d(0, -100%, 0);
    }
    
    a {
      display: block;
      width: 100px;
      height: 100px;
      position: relative;
      z-index: 400;
      margin: 0 auto 100px;
      top: 50px;
      transform: rotateX(55deg) scale(0);
      
      img {
        width: 100%;
        border-radius: 50%;
        box-shadow: 0px 2px 4px rgba(0,0,0,0.3);
      }
    }
    
    h1 {
      text-align: center;
      font-family: $roboto;
      padding: 15px 0 5px;
      margin: 0;
      font-weight: 400;
      color: black;
      font-size: 1.75rem;
      opacity: 0;
    }
    
    h2 {
      text-align: center;
      font-family: $roboto;
      line-height: 1.5;
      font-weight: 300;
      margin: 0 0 20px;
      padding: 0 10px;
      font-size: 1rem;
      color: #555;
      opacity: 0;
    }
  }
  
  .profile-bio {
    padding: 5px 20px;
    box-sizing: border-box;
    display: block;
    position: relative;
    opacity: 1;
    text-align: center;
    
    &:before {
      content: "";
      position: absolute;
      top: 0;
      left: 150px;
      rigth: 150px;
      width: 0px;
      height: 1px;
      background: black;
    }
    
    p {
      line-height: 1.5;
      font-size: .95rem;
      font-weight: 300;
      color: #666;
      opacity: 0;
    }
  }
  
  .profile-social-links {
    padding: 0 0 10px;
    list-style: none;
    text-align: center;
    
    li {
      display: inline-block;
      transform: scale(0);
      
      a {
        display: block;
        width: 30px;
        margin: 0 5px;
        
        img {
          width: 100%;
        }
      }
    }
  }
}

@keyframes bounce {
  from {
    top: 96%;
  }
  to {
    top: 85%;
  }
}

@keyframes shadow {
  from {
    height: 5px;
  }
  to {
    height: 15px;
    transform: scale(.5);
  }
}

.copyright {
  position: relative;
  bottom: -28%;
  left: 0;
  right: 0;
  text-align: center;
  font-family: "Roboto";
}
.copyright span {
  line-height: 36px;
  color: rgba(255, 255, 255, 0.75);
  font-weight: 300;
}
.copyright span a {
  font-weight: 400;
  text-decoration: none;
  color: #ea4c89;
}
.copyright .balapa {
  width: 30px;
  height: 30px;
  display: block;
  background: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/111167/profile/profile-512_4.jpg");
  background-size: cover;
  border-radius: 50%;
  border: 5px solid rgba(255, 255, 255, 0.75);
  float: right;
}
</style>