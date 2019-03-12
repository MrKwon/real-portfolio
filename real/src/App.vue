<template>
  <v-app>
    <div>
      <full-page ref="fullpage" :options="options" id="fullpage">
        <Main />
        <Profile />
        <History />
        <Portfolio />
        <Footer />
      </full-page>
    </div>
  </v-app>
</template>

<script>
import Main from '@/pages/Main'
import Profile from '@/pages/Profile'
import History from '@/pages/History'
// import Resume from '@/pages/Resume'
import Portfolio from '@/pages/Portfolio'
import Footer from '@/pages/Footer'

export default {
  name: "App",
  components: {
    Main,
    Profile,
    History,
    // Resume,
    Portfolio,
    Footer
  },
  data() {
    return {
      options: {
        menu: "#menu",
        anchors: ["index", "profile", "timeline", "portfolio", "footer"],
        sectionsColor: ["#3F3F3F", "#3F3F3F", "#3F3F3F","#3F3F3F", "#FFFFFF"],
        // lockAnchors: true,
        scrollBar: false,
        scrollOverflow: true,
        fitToSection: true,
        navigation: true,
        navigationPosition: 'right',
        navigationTooltips: ['Index', 'Profile', 'Timeline', 'Portfolio' ,'Thanks'],
        licenseKey: ''
      }
    };
  }
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
.section{
  text-align: center;
  color: aliceblue;
}

#fp-nav ul li a span, .fp-slidesNav ul li a span{ background: #fff !important; }
</style>
