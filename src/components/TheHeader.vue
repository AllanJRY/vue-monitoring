<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarTogglerDemo01"
      aria-controls="navbarTogglerDemo01"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
      <div class="w-100 d-flex justify-content-between align-items-center p-2">
        <a class="navbar-brand" href="#">Serveur Monitoring</a>
        <ul class="navbar-nav mr-auto mt-2 mt-lg-0">

        </ul>

        <ServersManager />
      </div>
    </div>
  </nav>
</template>

<script>
import ServersManager from "./ServersManager.vue";
export default {
  components: { ServersManager },
  name: "TheHeader",
};
</script>