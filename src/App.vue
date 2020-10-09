<template>
  <div>
    <!-- Component can use self-closing tag if we use PascalCase component -->
    <TheHeader />
    <BadgeList />
    <UserInfo
      :full-name="activeUser.name"
      :info-text="activeUser.description"
      :role="activeUser.role"
    ></UserInfo>
  </div>
</template>

<script>

import TheHeader from './components/TheHeader.vue'
import BadgeList from './components/BadgeList.vue';
import UserInfo from './components/UserInfo.vue';

export default {

  // locally registered components
  // this is a key-value pair but gets automatically registered if you provide one value
  components: {
    BadgeList,
    TheHeader,
    UserInfo
  },

  data() {
    return {
      activeUser: {
        name: 'Maximilian Schwarzmüller',
        description: 'Site owner and admin',
        role: 'admin',
      },
    };
  },
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