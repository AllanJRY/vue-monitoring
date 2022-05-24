<template>
  <div class="d-flex flex-column align-items-end">
    <p class="mb-1">
      Serveurs up : <span class="mx-2 text-success">{{ serverUp }}</span> 
      <button
        type="button"
        class="btn btn-outline-danger"
        title="Arrêter tous les serveurs up"
      >
        Stopper
      </button>
    </p>
    <p class="m-0">
      Serveurs down : <span class="mx-2 text-danger">{{ serverUp }}</span>
      <button
        type="button"
        class="btn btn-outline-warning"
        title="Relancer tous les serveurs down"
      >
        Relancer
      </button>
    </p>
  </div>
</template>

<script>
export default {
  name: "ServersManager",
  data() {
    return {
      serverUp: 0,
      serverDown: 0,
    };
  },
};
</script>

<style lang="scss" scoped>
p {
  color: white
}
</style>