<script lang="ts" setup >
import {computed} from "vue";

interface Props {
  isComplete: boolean
  name: string
}
const props = defineProps<Props>();

const emit = defineEmits(['update']);

const toggleStatus = () => {

}
const removeTask = () => {

}

const toggleButtonLabel = computed(() => props.isComplete ? 'B' : 'C')
</script>

<template>
  <div class="task-container">
    <div class="task-buttons-block">
      <button
        class="task-button"
        @click="toggleStatus"
       >
        {{ toggleButtonLabel }}
      </button>
      <button
        class="task-button"
        @click="removeTask"
      >
        R
      </button>
    </div>
    <div class="task-title">{{ name }}</div>
    <div class="task-status">{{ isComplete }}</div>

  </div>
</template>

<style lang="scss">
.task-container {
  width: 120px;
  height: 80px;
  border: 1px solid var(--divider);
  border-radius: 4px;
  padding: 4px;
  position: relative;
  display: flex;
  flex-direction: column;
  .task-buttons-block {
    display: flex;
    gap: 2px;
    align-self: end;

    .task-button {
      cursor: pointer;
      height: 20px;
      width: 20px;
      border-radius: 50%;
      border: 1px solid var(--divider);
      display: flex;
      justify-content: center;
      align-items: center;
      color: var(--text);
      font-size: 10px;

      &:hover {
        background-color: var(--primary-color);
      }
    }
  }
}
</style>
