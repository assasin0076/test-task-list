<script setup lang="ts">
import Task from "@/components/Task.vue";
import Header from "@/components/Header.vue";
</script>

<template>
  <div class="core-page">
    <Header />
    <div class="page-content">
      <Task name="aa" is-complete="true" />
    </div>
  </div>
</template>

<style lang="scss">


.core-page {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  padding: 2rem;
  gap: 20px;

  .page-content {
    background-color: var(--light-primary-color);
    border: 1px solid var(--divider);
    border-radius: 4px;
    flex: 1;
    padding: 8px;
  }
}
</style>
