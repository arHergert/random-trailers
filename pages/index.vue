<template>
  <div>
    <v-app>
      <v-layout>
        <v-flex md11><VideoPlayer /></v-flex>
        <v-flex md3><ConfigTabs /> </v-flex>
      </v-layout>
      <v-snackbar
        right
        :height="350"
        :timeout="this.$store.state.snackbarTimeout"
        :value="this.$store.state.snackbarShow"
        :color="this.$store.state.snackbarColor"
      >
        <div class="snackbar">
          <span class="snackbar-icon">
            {{ this.$store.state.snackbarIcon }}
          </span>
          <span class="snackbar-text">
            {{ this.$store.state.snackbarText }}
          </span>
        </div>
      </v-snackbar>
    </v-app>
  </div>
</template>

<script>
import ConfigTabs from '~/components/tabs/ConfigTabs.vue'
import VideoPlayer from '~/components/videoPlayer/VideoPlayer'

export default {
  ConfigTabs,
  VideoPlayer,
  data() {
    return {}
  },
  methods: {}
}
</script>

<style lang="scss">
.v-snack {
  bottom: 25px;
  right: 43px;
}

.snackbar {
  span {
    vertical-align: middle;
  }
}

.snackbar-icon {
  font-size: 30px;
  margin-right: 7px;
}

.snackbar-text {
  font-weight: 600;
  font-size: 16px;
}

.theme--light.v-application {
  background: black;
}
</style>
