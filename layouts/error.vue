<template>
  <div>Error page: {{ headers }}</div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { useNuxtApp, useState } from "#app";

export default defineComponent({
  props: {
    error: Object,
  },
  setup() {
    const { ssrContext } = useNuxtApp();
    const headers = useState("headers", () => ssrContext?.req.headers);
    return { headers };
  },
});
</script>
