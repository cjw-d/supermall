<template>
  <div id="tab-bar">
    <slot></slot>
  </div>
</template>

<script>
export default {};
</script>

<style>
#tab-bar {
  display: flex;

  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;

  background-color: #f6f6f6;

  box-shadow: 0 -3px 1px rgba(100, 100, 100, 0.3);
}
</style>