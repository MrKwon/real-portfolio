<template>
  <v-app>
    <div>
      <full-page ref="fullpage" :options="options" id="fullpage">
        <Main />
        <Resume />
        <Portfolio />
        <Footer />
      </full-page>
    </div>
  </v-app>
</template>

<script>
import Main from '@/components/pages/Main'
import Resume from '@/components/pages/Resume'
import Portfolio from '@/components/pages/Portfolio'
import Footer from '@/components/pages/Footer'

export default {
  name: "App",
  components: {
    Main,
    Resume,
    Portfolio,
    Footer
  },
  data() {
    return {
      options: {
        menu: "#menu",
        anchors: ["index", "skill", "portfolio", "footer"],
        sectionsColor: ["#3F3F3F", "#3F3F3F", "#3F3F3F", "FFFFFF"],
	      lockAnchors: true,
        navigation: true,
        navigationPosition: 'right',
        navigationTooltips: ['Index', 'Skill', 'Portfolio', 'Thanks'],
	      showActiveTooltip: true,
        slidesNavigation: true,
        verticalCentered: true,
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
</style>
