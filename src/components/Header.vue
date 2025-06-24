<template>
  <div class="page-header">
    <div class="add-task-block">
      <input class="add-task-input" type="text" placeholder="task">
      <button class="add-task-button">add</button>
    </div>
  </div>
</template>

<style lang="scss">
.page-header {
  width: 100%;
  height: 40px;
  background-color: var(--light-primary-color);
  border: 1px solid var(--divider);
  border-radius: 4px;
  padding: 8px;

  .add-task-block {
    display: flex;
    gap: 8px;
    .add-task-input {
      width: 120px;
      height: 20px;
      border: 1px solid var(--divider);
      border-radius: 4px;
      padding: 4px;
      font-size: 12px;
    }

    .add-task-button {
      cursor: pointer;
      height: 20px;
      width: 40px;
      border-radius: 4px;
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
