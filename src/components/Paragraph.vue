<template>
  <p>
    <component :is="prefix.component" v-bind="prefix.props"></component>
    <slot></slot>
  </p>
</template>
<script>
export default {
  props: {
    prefix: {
      validator: v => {
        return v.component && v.props;
      }
    }
  }
};
</script>
