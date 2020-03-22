<template>
  <div class="home">
    <div class="grid  grid-cols-2 sm:grid-cols-3 gap-4">
      <div class="max-w-sm rounded overflow-hidden shadow-lg bg-white hover:shadow-outline cursor-pointer"
           style="cursor:pointer"
           @click="redirectTo('homepriceheatmap')"
      >
        <img class="w-full" src="../assets/img/priceHeatmap.png" alt="home price heatmap">
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">Home Price Heatmap</div>
          <p class="text-gray-700 text-base">
            See home prices around the home you are trying to buy.
          </p>
        </div>
      </div>
      <div class="max-w-sm rounded overflow-hidden shadow-lg bg-white hover:shadow-outline"
           style="cursor:pointer"
           @click="redirectTo('neighbohoodcrimeheatmap')"
      >
        <img class="w-full" src="../assets/img/crimeHeatmap.png" alt="neighborhood crime">
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">Neighborhood Crime Heatmap</div>
          <p class="text-gray-700 text-base">
              See neighborhood crime for the home you are trying to buy.
          </p>
        </div>
      </div>
      <div class="max-w-sm rounded overflow-hidden shadow-lg bg-white hover:shadow-outline"
           style="cursor:pointer"
           @click="redirectTo('basicstreetmap')"
      >
        <img class="w-full" src="../assets/img/sampleMap.png" alt="normal map">
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">Normal Map</div>
          <p class="text-gray-700 text-base">
            Just see a normal map around my next home.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HomePriceHeatmap from '@/views/HomePriceHeatmap.vue'

export default {
  name: 'Home',
  components: {
  },
  methods: {
    redirectTo(routeName) {
      this.$router.push(
              {
                path: '/' + routeName
              }
      )
    }
  }
}
</script>

<style scoped xml:lang="scss">

</style>
