<template>
  <section>
    <base-card>
      <header>
        <h3>{{ fullName }}</h3>
        <base-badge :type="role" :caption="role.toUpperCase()"></base-badge>
      </header>
      <p>{{ infoText }}</p>
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