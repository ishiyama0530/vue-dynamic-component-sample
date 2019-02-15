<template>
  <div>
    <Paragraph :prefix="{ component: prefix, props: prefixProps }">
      sample
    </Paragraph>
  </div>
</template>

<script>
import Paragraph from "./components/Paragraph.vue";
import Prefix from "./components/Prefix.vue";

export default {
  name: "app",
  components: {
    Paragraph
  },
  data: () => {
    return { prefix: Prefix, prefixProps: { mark: "*", color: "blue" } };
  }
};
</script>
