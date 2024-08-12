<template>
    <div class="Activity-tl-container">
      <h2>Activity Timeline</h2>
      <ul>
        <li v-for="activity in activities" :key="activity.time">
          <span class="time">{{ activity.time }}</span>
          <span class="activity">{{ activity.activity }}</span>
          <span class="description">{{ activity.description }}</span>
          <a v-if="activity.link" :href="activity.link" class="pdf-link">{{ activity.linkText }}</a>
          <span v-if="activity.client" class="client">{{ activity.client }}</span>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: "ActivityTimeline",
    props: {
      activities: {
        type: Array,
        required: true,
      },
    },
  };
  </script>
  