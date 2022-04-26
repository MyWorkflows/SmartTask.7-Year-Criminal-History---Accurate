<script lang="ts">
import { defineComponent } from "vue";


export default /*#__PURE__*/ defineComponent({
  name: "SmartTaskComponent", // vue component name
  props: ['componentState', 'componentStatus'],
  data() {
    return { model: {} };
  },
  computed: {},
  methods: {
    async submitForm() {
      this.$emit("execute-smart-task", this.model);
    },
  },
  created() {
    if (this.componentState) {
      this.model = this.componentState;
    }
  },
  setup() {},
});
</script>

<template>
  <form>
    <div class="my-5">
      <button
        type="button"
        @click="submitForm"
        class="btn btn-sm btn-primary"
      >
       Mark as in Progress
      </button>
    </div>
  </form>
</template>

