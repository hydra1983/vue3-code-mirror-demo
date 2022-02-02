<template>
  <v-code-mirror
      v-model:value="content"
      lang="html"
      theme="chrome"
      style="height: 300px"/>
</template>

<script lang="ts">
import CodeMirror from 'codemirror';
import {VCodeMirror} from "vue3-code-mirror";
import 'codemirror/mode/yaml/yaml';
export default {
  name: "app",
  data: () => ({
    content: "",
    mode: "text/x-yaml"
  }),
  mounted: () => {
    console.log(CodeMirror.modes);
    console.log(CodeMirror.mimeModes);
  },
  components: {
    VCodeMirror
  }
};
</script>
