<template>
  <base-card>
    <base-button @click="setSelectedTab('stored-resources')"
      >Stored Resources</base-button
    >
    <base-button @click="setSelectedTab('add-resource')"
      >Add Resource</base-button
    >
  </base-card>

  <!-- <stored-resources
    v-if="selectedTab === 'stored-resources'"
  ></stored-resources>
  <add-resource v-if="selectedTab === 'add-resource'"></add-resource> -->

  <keep-alive>
    <component :is="selectedTab"></component>
  </keep-alive>
</template>

<script>
import AddResource from './AddResource.vue';
import StoredResources from './StoredResources.vue';
export default {
  components: { StoredResources, AddResource },
  data() {
    return {
      selectedTab: 'stored-resources',
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
  provide() {
    return {
      resources: this.storedResources, // we are providing all resources to low level component or child component or his child component
    };
  },
  methods: {
    setSelectedTab(tab) {
      console.log('activated ' + tab);
      this.selectedTab = tab;
    },
  },
};
</script>
