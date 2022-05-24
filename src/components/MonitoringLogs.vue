<template>
  <div class="container monitoring-logs">
    <div class="row">
      <div class="col-12">
        <h2>les logs</h2>
      </div>
    </div>
    <div class="row logs">
      <p
        v-for="log in logs"
        :key="log.id"
        class="col-12"
        :class="{
          'text-muted': 'info' == log.level,
          'text-warning': 'warning' == log.level,
        }"
      >
        {{ log.msg }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "MonitoringLogs",
  data() {
    return {
      logs: [
        {
          id: 56,
          level: "info",
          msg: "[Info] server 1 started",
        },
        {
          id: 123,
          level: "info",
          msg: "[Info] server 2 started",
        },
        {
          id: 43,
          level: "warning",
          msg: "[Warning] server 3 stopped",
        },
        {
          id: 35,
          level: "info",
          msg: "[Info] server 4 started",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.monitoring-logs .logs {
  border: 1px solid black;
  border-radius: 7px;
  padding: 1rem;
}
</style>