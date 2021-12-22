<template>
  <div class="bg-gray-900 h-screen">
    <h1 class="text-red-800">qualquer coisa</h1>
    <div class="cards">
      <TrackCard
        v-for="(track, index) in tracks"
        :key="index"
        :name="track.trackName"
        :icon="track.icon"
        :duration="track.durationInWeeks"
        :completitionState="track.trackCompletitionState"
      />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TrackCard from '@/components/molecules/TrackCard.vue'

interface Track {
  trackName: string
  icon: string
  durationInWeeks: number
  trackCompletitionState: string
}

export default Vue.extend({
  name: 'IndexPage',
  components: { TrackCard },
  data() {
    return {
      tracks: [
        {
          trackName: 'backend:C#',
          icon: 'csharp.png',
          durationInWeeks: 12,
          trackCompletitionState: '2/4',
        },
        {
          trackName: 'iOS:swift',
          icon: '',
          durationInWeeks: 10,
          trackCompletitionState: '1/4',
        },
        {
          trackName: 'DevOps:go',
          icon: '',
          durationInWeeks: 12,
          trackCompletitionState: '2/4',
        },
        {
          trackName: 'data:Python',
          icon: '',
          durationInWeeks: 12,
          trackCompletitionState: '2/4',
        },
      ] as Track[],
    }
  },
})
</script>

<style scoped>
body {
  width: 100vh;
  height: 100vh;
}
.cards {
  margin: 0 auto;
  display: flex;
  justify-content: space-around;
}
</style>
