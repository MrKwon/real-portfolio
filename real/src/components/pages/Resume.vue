<template>
  <v-container height="100%">
    <v-layout class="layout_resume"  pa-4 row>
      <v-flex class="timeline" xs6>
        <Timeline />
      </v-flex>
      <v-flex xs6>
        <Skills />
      </v-flex>
    </v-layout>
  </v-container>
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