<template>
  <div class="card">
    <p class="card-title">[{{ name }}]</p>
    <div class="icon">
      <img src="../../assets/images/icons/csharp.svg" />
    </div>
    <div class="track-info">
      <p>{{ duration }} weeks</p>
      <p>{{ completitionState }} completed</p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'Vue'

export default Vue.extend({
  name: 'TrackCard',
  props: {
    name: String,
    icon: String,
    duration: Number,
    completitionState: String,
  },
})
</script>

<style scoped>
.card {
  background-color: #0760e0;
  width: 325px;
  height: 325px;
}

p {
  font-family: DM Mono;
  font-style: normal;
  font-weight: 500;
  font-size: 15px;
  line-height: 20px;
}

.card-title {
  padding: 4px;
  margin-left: 8px;
}

.icon img {
  width: 100%;
  margin: 0 auto;
  height: 250px;
}

.track-info {
  display: flex;
  justify-content: space-between;
  padding: 8px;
}
</style>