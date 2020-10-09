<template>
  <section>
    <base-card>
      <!-- use v-slot directive tells Vue where content should go
      v-slot:header is long form
      #header is shorthand for 'v-slot:header'
      -->
      <template #header>
        <h3>{{ fullName }}</h3>
        <base-badge :type="role" :caption="role.toUpperCase()"></base-badge>
      </template>

      <template #default>
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