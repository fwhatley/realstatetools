<template>
  <div class="map-container">
    <MglMap :accessToken="accessToken"
            :mapStyle="mapStyle"
            @load="onMapLoaded"
    />
  </div>

</template>

<script>
  import { MglMap } from "vue-mapbox";

  export default {
    components: {
      MglMap
    },
    data() {
      return {
        accessToken: "pk.eyJ1IjoiZnJlZHl3aGF0bGV5IiwiYSI6ImNrNnNtdG1jbzA0cnIza3I0azdlNTY0a2YifQ.QASUZO4iouN_ymJXMEfEpQ",
        mapStyle: "mapbox://styles/fredywhatley/ck83fm2h21e2y1il82u8qwmcp"
      };
    },

    created() {
      this.map = null;
    },
    methods: {
      async onMapLoaded(event) {
        this.map = event.map;
      }
    }
  };
</script>

<style scoped xml:lang="scss">
  .map-container {
    height: 800px;
  }
</style>
