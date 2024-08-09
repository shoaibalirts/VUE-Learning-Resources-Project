<template>
  <the-header title="RememberMe"></the-header>
  <stored-resources :stored-resources="storedResources"></stored-resources>
</template>

<script>
import TheHeader from './components/layouts/TheHeader.vue';
import StoredResources from './components/StoredResources.vue';

export default {
  components: {
    StoredResources,
    TheHeader,
  },
  data() {
    return {
      storedResources: [
        {
          id: 'Official Guide',
          title: 'Official Guide',
          description: 'The official Vue.js documentation',
          link: 'https://vuejs.org',
        },
        {
          id: 'Google',
          title: 'Google',
          description: 'Learn to google...',
          link: 'https://learning.google/',
        },
      ],
    };
  },
  methods: {},
};
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>
