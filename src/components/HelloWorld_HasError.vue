<template>
  <editor-content :editor="editor" />
</template>

<script lang="ts">
import { Editor, EditorContent } from "@tiptap/vue-3";
import StarterKit from "@tiptap/starter-kit";
import { defineComponent } from "vue";

export default defineComponent({
  components: {
    EditorContent
  },

  data() {
    return {
      editor: new Editor({
        content: "<h2>I throw an error. 🐛</h2>",
        extensions: [StarterKit]
      })
    };
  },

  mounted() {},

  beforeUnmount() {
    this.editor.destroy();
  }
});
</script>
