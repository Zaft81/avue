<template>
  <el-cascader :options="dic"
               v-model="text"
               :placeholder="placeholder"
               :props="props"
               :readonly="readonly"
               :size="size"
               :change-on-select="changeOnSelect"
               :clearable="disabled?false:clearable"
               :expand-trigger="expandTrigger"
               :show-all-levels="showAllLevels"
               :filterable="filterable"
               :separator="separator"
               :disabled="disabled"
               @click.native="handleClick"
               @change="handleChange"></el-cascader>
</template>

<script>
import create from "core/create";
import props from "../../core/common/props.js";
import event from "../../core/common/event.js";
export default create({
  name: "cascader",
  mixins: [props(), event()],
  props: {
    value: {
      type: Array,
      default: () => []
    },
    changeOnSelect: {
      type: Boolean,
      default: false
    },
    expandTrigger: {
      type: String,
      default: "hover"
    },
    showAllLevels: {
      type: Boolean,
      default: true
    },
    filterable: {
      type: Boolean,
      default: false
    },
    separator: {
      type: String,
      default: "/"
    }
  },
  data () {
    return {};
  },
  watch: {},
  created () { },
  mounted () { },
  methods: {}
});
</script>
