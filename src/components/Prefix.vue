<template>
  <span :style="{ color: color }">{{ mark }}</span>
</template>
<script>
export default {
  props: ["mark", "color"]
};
</script>
