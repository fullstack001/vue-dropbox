<template>
  <div>
    <VueDropboxPicker
        class="cloud dropbox"
        :api-key="''"
        link-type="direct"
        :multiselect="true"
        :extensions="['.pdf', '.doc']"
        :folderselect="false"
        @cancel="onCancelDropbox"
        @picked="onPickedDropbox">
      <span>Open Dropbox Picker</span>
    </VueDropboxPicker>
  </div>
</template>

<script>


import VueDropboxPicker from './components/DropboxPicker.vue'

export default {
  name: 'App',
  methods: {
    onCancelDropbox (data) {
      window.console.log('on cancel:', data)
    },
    onPickedDropbox (data) {
      window.console.log('on picked:', data)

    }
  },
  components: {
    VueDropboxPicker
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
