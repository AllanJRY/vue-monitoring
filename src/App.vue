<template>
  <div id="app">
    <TheHeader />
    <ServerList />
    <MonitoringLogs />
  </div>
</template>

<script>
import MonitoringLogs from './components/MonitoringLogs.vue'
import ServerList from './components/ServerList.vue'
import TheHeader from './components/TheHeader.vue'

export default {
  components: {
    TheHeader,
    ServerList,
    MonitoringLogs,

  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
