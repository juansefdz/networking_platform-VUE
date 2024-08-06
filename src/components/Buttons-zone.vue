<template>
  <div class="container-buttons">
    <div
      v-for="(button, index) in buttons"
      :key="index"
      class="button-container"
      :class="{ selected: selectedButton === index }"
      @click="selectButton(index)"
    >
      <i :class="button.icon"></i>
      <button class="button">{{ button.label }}</button>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const selectedButton = ref(0);
    const buttons = ref([
      { label: "Profile", icon: "bx bxs-user" },
      { label: "Team", icon: "bx bx-group" },
      { label: "Projects", icon: "bx bx-spreadsheet" },
      { label: "Connections", icon: "bx bx-at" },
    ]);

    const selectButton = (index) => {
      selectedButton.value = index;
    };

    return {
      selectedButton,
      buttons,
      selectButton,
    };
  },
};
</script>

<style scoped>
.container-buttons {
  display: flex;
  gap: 10px;
  margin-top: 20px;
  align-items: center;
}

.button-container {
  display: flex;
  align-items: center;
  gap: 5px;
}

.container-buttons button {
  background-color: #f5f5f5;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  font-size: 16px;
  font-weight: 500;
  color: #fff;
  cursor: pointer;
  transition: all 0.3s ease;
}

.button-container.selected button {
  background: #780b74;
}

.button-container:not(.selected) button {
  background: #f5f5f5;
  color: #000;
}
</style>
