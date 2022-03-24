<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  data() {
    return {
      isChecked: false,
    };
  },
  computed: {
    slider() {
      if (this.isChecked) {
        return "absolute bg-gray-700 shadow-lg border-2 border-green-300 w-[1.75rem] h-[1.75rem] rounded-xl";
      } else {
        return "absolute bg-gray-700 shadow-lg border-2 border-red-300 w-[1.75rem] h-[1.75rem] rounded-xl";
      }
    },
  },
});
</script>

<template>
  <span class="flex">
    <input
      type="checkbox"
      class="appearance-none peer bg-gray-600 rounded-xl w-[5rem] h-[2.25rem] border-2 border-gray-500"
      v-model="isChecked"
    />
    <span
      class="group absolute flex flex-col w-[5rem] h-[2.2rem] p-1 justify-center pointer-events-none transition-transform duration-300 peer-checked:translate-x-11"
    >
      <span :class="slider" />
    </span>
  </span>
</template>
