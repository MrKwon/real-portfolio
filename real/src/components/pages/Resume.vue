<template>
  <div class="section">
    <div class="fp-tableCell">
      <v-container class="resume" fluid>
        <v-layout pr-4 pl-4 row>
          <v-flex class="timeline" xs6>
            <Timeline />
          </v-flex>
          <v-flex xs6>
            <Skills />
          </v-flex>
        </v-layout>
      </v-container>
    </div>
  </div>
</template>

<script>
import Timeline from '@/components/Timeline'
import Skills from '@/components/Skills'

export default {
  data () {
    return {

    }
  },
  components: {
    Timeline,
    Skills
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.timeline {
  height: 100%;
}
</style>