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
    <!-- scoped slot: allows us to STYLE content
      don't need template wrapper if all markup can go into one slot
    -->
    <course-goals #default="slotProps">
      <h2> {{ slotProps.item }}</h2>
      <p>{{ slotProps['another-prop'] }}</p>
    </course-goals>
  </div>
</template>

<script>

import TheHeader from './components/TheHeader.vue'
import BadgeList from './components/BadgeList.vue';
import UserInfo from './components/UserInfo.vue';
import CourseGoals from './components/CourseGoals.vue';

export default {

  // locally registered components
  // this is a key-value pair but gets automatically registered if you provide one value
  components: {
    BadgeList,
    TheHeader,
    UserInfo,
    CourseGoals
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