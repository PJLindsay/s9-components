<template>
  <section>
    <base-card>
      <!-- use v-slot directive tells Vue where content should go -->
      <template v-slot:header>
        <h3>{{ fullName }}</h3>
        <base-badge :type="role" :caption="role.toUpperCase()"></base-badge>
      </template>

      <template v-slot:default>
        <p>{{ infoText }}</p>
      </template>
    </base-card>
  </section>
</template>

<script>
export default {
  props: ['fullName', 'infoText', 'role'],
};
</script>

<!-- scoped tells Vue to only affect this template (not global) -->
<style scoped>

section header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>