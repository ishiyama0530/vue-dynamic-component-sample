<template>
  <div>
    <Paragraph :prefix="prefix">sample</Paragraph>
    <button @click="onclickA">switch_a</button>
    <button @click="onclickB">switch_b</button>
  </div>
</template>

<script>
import Paragraph from "./components/Paragraph.vue";
import PrefixA from "./components/PrefixA.vue";
import PrefixB from "./components/PrefixB.vue";

export default {
  name: "app",
  components: {
    Paragraph
  },
  data: () => {
    return {
      prefix: {
        component: PrefixA,
        props: {
          mark: "?"
        }
      }
    };
  },
  methods: {
    onclickA() {
      this.prefix.component = PrefixA;
      this.prefix.props.mark = "+";
    },
    onclickB() {
      this.prefix.component = PrefixB;
      this.prefix.props.mark = "-";
      this.prefix.props.color = "red";
    }
  }
};
</script>
