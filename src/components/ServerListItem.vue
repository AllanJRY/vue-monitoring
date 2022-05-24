<template>
  <div class="server-card">
    <p>{{ name }}</p>
    <p
      :class="{
        'text-success': 'up' == status,
        'text-danger': 'down' == status,
      }"
    >
      {{ status }}
    </p>
      <button
        type="button"
        class="btn"
        :class="{
            'btn-outline-danger': 'up' == status,
            'btn-outline-success': 'down' == status,
        }"
      >
        {{ btnLabel }}
      </button>
  </div>
</template>

<script>
export default {
  name: "ServerListItem",
  props: {
    name: {
      type: String,
      required: true,
    },
    status: {
      type: String,
      required: true,
    },
  },
  computed: {
      btnLabel() {
          if('up' == this.status) return 'Arrêter';

          if('down' == this.status) return 'Lancer';
          
          return 'Unknown'
      }
  }
};
</script>

<style lang="scss" scoped>
.server-card {
  border: 1px solid black;
  border-radius: 7px;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>