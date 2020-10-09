<template>
  <div>
    <!-- Component can use self-closing tag if we use PascalCase component -->
    <TheHeader />

    <button @click="setSelectedComponent('active-goals')">Active Goals</button>
    <button @click="setSelectedComponent('manage-goals')">Manage Goals</button>

    <!-- keep-alive allows vue not to remove/delete input field data if we swap component -->
    <!-- dynamic component placeholder: allows us to swap-in/swap out ANY component! -->
    <keep-alive>
      <component :is="selectedComponent"></component>
    </keep-alive>

  </div>
</template>

<script>

import TheHeader from './components/layout/TheHeader.vue'
// import BadgeList from './components/BadgeList.vue';
// import UserInfo from './components/UserInfo.vue';
// import CourseGoals from './components/CourseGoals.vue';

import ActiveGoals from './components/ActiveGoals.vue';
import ManageGoals from './components/ManageGoals.vue';

export default {

  // locally registered components
  // this is a key-value pair but gets automatically registered if you provide one value
  components: {
    ActiveGoals,
    // BadgeList,
    TheHeader,
    // UserInfo,
    // CourseGoals,
    ManageGoals
  },

  data() {
    return {
      activeUser: {
        name: 'Maximilian Schwarzmüller',
        description: 'Site owner and admin',
        role: 'admin',
      },
      selectedComponent: 'active-goals'
    }
  },

  methods: {
    setSelectedComponent(comp) {
      this.selectedComponent = comp
    }
  }
};
</script>

<!-- typically Global styles go here -->
<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>