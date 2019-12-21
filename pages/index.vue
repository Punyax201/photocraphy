<template>
<v-container fluid>

  <!---->
  <Selector v-on:click.native="a" class="mx-auto"/>
  <v-layout
    justify-center
    align-center
    id="main"
  >
    <v-flex lg12 md12>
      <!--TIMELINE VIEW-->
      <v-scale-transition>
        <Timeline v-if="timelineActive" />
      </v-scale-transition>

      <!--GRID VIEW-->
      <v-scale-transition>
        <Grid v-if="!timelineActive" />
      </v-scale-transition>
    </v-flex>
  </v-layout>
</v-container>
</template>
<script>
/* eslint-disable */
import Timeline from '@/components/Timeline'
import Selector from '@/components/ModeSelector'
import Grid from '@/components/Grid'

export default {
  components: {
    Timeline,
    Selector,
    Grid
  },
  data () {
    return {
      timelineActive: false,
      tri: this.$store.state.imageData.x
    }
  },
  methods:{
    a:function(event){
      this.timelineActive = !this.timelineActive
    }
  }
}
</script>

<style>
</style>
