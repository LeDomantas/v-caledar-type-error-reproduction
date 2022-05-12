<script setup lang="ts">
import { DatePicker } from "v-calendar";
import { ref } from "vue";

const date = ref();
</script>

<template>
  <DatePicker v-model="date" :columns="$screens({ xs: 1, sm: 2 })">
    <template v-slot="{ inputValue, inputEvents }">
      <input
        class="bg-white border px-2 py-1 rounded"
        :value="inputValue"
        v-on="inputEvents"
      />
    </template>
  </DatePicker>
</template>