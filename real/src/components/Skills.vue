<template>
    <v-layout column mt-2 mb-2 mr-2 ml-4>
      <v-card align-center>
        <v-subheader>Language</v-subheader>
        <v-container fluid grid-list-sm>
          <v-layout row wrap>
            <v-flex xs3
              v-for="(item, i) in language"
              :key="i">
              <img
                :src="`@/assets/logo/${item.name}_256x256.png`"
                class="image" :alt="`${item.name}`" width="100%" height="100%">
            </v-flex>
          </v-layout>
        </v-container>
        <v-subheader>Web and App Skill</v-subheader>
        <v-container fluid grid-list-sm>
          <v-layout row wrap>
            <v-flex xs3
              v-for="(item, i) in webapp"
              :key="i">
              <img
                :src="`@/assets/logo/lang/${item.name}_256x256.png`"
                class="image" :alt="`${item.name}`" width="100%" height="100%">
            </v-flex>
          </v-layout>
        </v-container>
        <v-subheader>Operating System</v-subheader>
        <v-container fluid grid-list-sm>
          <v-layout row wrap>
            <v-flex xs3
              v-for="(item, i) in os"
              :key="i">
              <img
                :src="`@/assets/logo/lang/${item.name}_256x256.png`"
                class="image" :alt="`${item.name}`" width="100%" height="100%">
            </v-flex>
          </v-layout>
        </v-container>
      </v-card>
    </v-layout>
</template>

<script>
export default {
  data () {
    return {
      language: [
        { name: "c" },
        { name: "cpp" },
        { name: "java" },
        { name: "kotlin" },
        { name: "javascript" },
      ],
      webapp: [
        { name: "android" },
        { name: "css" },
        { name: "html" },
        { name: "vue" },
        { name: "react" },
        { name: "node" },
      ],
      os: [
        { name: "windows" },
        { name: "linux" },
        { name: "mac" },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url(https://fonts.googleapis.com/css?family=Poppins:400);

.title_profile {
  position: relative;
  font-size: 40px ;
  font-family: 'Poppins', sans-serif !important;
  font-weight: 400 !important;
  top: 8%;
  padding-bottom: 2vh;
}
</style>