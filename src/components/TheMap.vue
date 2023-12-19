<script lang="ts" setup>
import * as mars3d from 'mars3d'
import 'mars3d/dist/mars3d.css'

onMounted(() => {
  const options: any = {
    basemaps: [
      {
        name: '天地图影像',
        icon: 'img/basemaps/tdt_img.png',
        type: 'tdt',
        layer: 'img_d',
        show: true,
      },
    ],
  }
  const map = new mars3d.Map('mars3dContainer', options)
  map.flyHome()
})
</script>

<template>
  <div id="mars3dContainer" />
</template>

<style scoped>
#mars3dContainer {
  position: absolute;
  height: 100%;
  width: 100%;
}
</style>
