<template>
  <div>

    <!-- slots allow us to receive HTML content (incl Vue features) from outside component
    in this case we provide styling for any components wrapped in a BaseCard
    -->

    <!-- use v-if so we don't have empty HTML elements (header) -->
    <header v-if="$slots.header">
      <slot name="header">
        <!-- we can add default/fallback content here (shown if content is not passed in) -->
        <!-- <h2>The Default</h2> -->
      </slot>
    </header>

    <!-- you can leave one slot unnamed: this will be default slot -->
    <slot></slot>
  </div>
</template>

<script>
  export default {
    mounted() {
      // console.log(this.$slots.header)
    }
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