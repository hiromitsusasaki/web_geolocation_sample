<template>
  <section>
    <div class="container">
      <div class="columns">
        <div class="column has-text-centered">
          <h1 style="margin-top: 24px;" class="is-size-2">geolocation sample</h1>
          <div style="height: 128px;">
            <p style="margin-top: 48px;">現在地: 緯度: {{lat}}  軽度: {{long}}</p>
          </div>
          <button type="button" class="button" v-on:click="watchLocation()">位置情報の取得を開始する</button><br />
          <button style="margin-top:48px" type="button" class="button" v-on:click="finishLocation()" >位置情報の取得を終了する</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Geolocation',
  data: function () {
    return {
      long: 0,
      lat: 0,
      watchId: null,
    }
  },
  methods: {
    watchLocation: function () {
      this.watchId = navigator.geolocation.watchPosition((position) => {
        this.lat = position.coords.latitude
        this.long = position.coords.longitude
      })
    },
    finishLocation: function () {
      navigator.geolocation.clearWatch(this.watchId);
    }
  }
}
</script>

<style scoped>

</style>
