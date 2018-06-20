<template>
  <div id="gismap" v-initmap>
  </div>
</template>
<script>
import Map from "ol/map";
import View from "ol/view";
import TileLayer from "ol/layer/tile";
import XYZ from "ol/source/xyz";
import "ol/ol.css";
export default {
  name: "gismap",
  directives: {
    initmap: {
      inserted: function() {
        new Map({
          target: "gismap",
          layers: [
            new TileLayer({
              source: new XYZ({
                url: "https://{a-c}.tile.openstreetmap.org/{z}/{x}/{y}.png"
              })
            })
          ],
          view: new View({
            center: [0, 0],
            zoom: 2
          })
        });
      }
    }
  }
};
</script>
