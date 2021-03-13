<template>
  <div class="home">
<yandex-map
:coords="[55.753215, 37.622504]" zoom="10"
style=" width: 100%; height: 986px; padding: 0; margin: 0;"
:cluster-options="{
    1: {clusterDisableClickZoom: true}
  }"
  :controls="['trafficControl']"
  :placemarks="placemarks">
    <ymap-marker marker-type="placemark"
      :coords="[55.753215, 37.622504]" hint-content="Hint content 1"
      :balloon="{header: 'header', body: 'body', footer: 'footer'}"
      :icon="{color: 'green', glyph: 'cinema'}"
      cluster-name="1"
    ></ymap-marker>
</yandex-map>
  </div>
</template>

<script>
import Vue from 'vue';
import YmapPlugin from 'vue-yandex-maps';

const settings = {
  apiKey: '2e778f7f-c5b1-462e-bf51-f543c3729d56',
  lang: 'ru_RU',
  coordorder: 'latlong',
  version: '2.1',
};
Vue.use(YmapPlugin, settings);

export default {
  name: 'Home',
  components: {
  },
};
</script>
