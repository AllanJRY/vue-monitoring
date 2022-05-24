<template>
  <div class="container my-3">
    <div class="row">
      <div class="col-12">
        <h2>Les serveurs</h2>
      </div>
    </div>
    <div class="row">
      <div
        class="col-12 col-md-6 col-lg-4 mb-3"
        v-for="server in servers"
        :key="server.name"
      >
        <ServerListItem :name="server.name" :status="server.status" />
      </div>
    </div>
  </div>
</template>

<script>
import ServerListItem from "./ServerListItem.vue";
export default {
  components: { ServerListItem },
  name: "ServerList",
  data() {
    return {
      servers: [
        {
          name: "Serveur 1",
          status: "up",
        },
        {
          name: "Serveur 2",
          status: "up",
        },
        {
          name: "Serveur 3",
          status: "down",
        },
        {
          name: "Serveur 4",
          status: "up",
        },
      ],
    };
  },
};
</script>