<template>
  <span :style="{ color }">(B){{ mark }}</span>
</template>
<script>
export default {
  inheritAttrs: false,
  props: ["mark", "color"]
};
</script>
