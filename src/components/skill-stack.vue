<script setup>
defineProps({
  header: {
    type: String,
    required: true,
  },
  items: {
    type: Array,
    required: true,
  },
  background: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <h4>{{ header }}</h4>
  <div class="stack-horizontal">
    <div
      v-for="skill in items"
      :key="skill"
      class="skillitem"
      :style="{ backgroundColor: background }"
    >
      {{ skill }}
    </div>
  </div>
</template>

<style scoped>
.skillitem {
  transition-duration: 0.2s;
  border-radius: 9999px;
  padding-left: 12px;
  padding-right: 12px;
  padding-top: 5px;
  padding-bottom: 5px;
  cursor: default;
}
.skillitem:hover {
  filter: brightness(1.2);
  transform: scale(1.15);
  box-shadow: 0px 1.5px 7px 0.5px rgba(255, 255, 255, 0.2);
}

h4 {
  margin-top: 20px;
  margin-bottom: 10px;
}
</style>
