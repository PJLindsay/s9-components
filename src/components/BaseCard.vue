<template>
  <div>

    <!-- slots allow us to receive HTML content (incl Vue features) from outside component
    in this case we provide styling for any components wrapped in a BaseCard
    -->
    <header>
      <slot name="header"></slot>
    </header>

    <!-- you can leave one slot unnamed: this will be default slot -->
    <slot></slot>
  </div>
</template>

<script>
  export default {
  }
</script>

<!-- scoped tells Vue to only affect this template (not global) -->
<style scoped>

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

div {
  margin: 2rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
}

</style>