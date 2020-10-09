<template>
  <ul>
    <li v-for="goal in goals" :key="goal">
      <!-- scoped slot - we can pass this out so callers can have access to the goal for custom styling/etc -->
      <slot :item="goal" another-prop="..."></slot>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      goals: ['Finish the course', 'Learn Vue'],
    }
  }
}
</script>