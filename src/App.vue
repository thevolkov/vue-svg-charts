<template>
  <div>
    <LabeledInput
      :input-label="'Value'"
      :input-type="'text'"
      v-model="inputValue"
    />
    {{ inputValue }}
  </div>
</template>

<script>
import LabeledInput from '@/components/LabeledInput.vue';

export default {
  name: 'App',
  components: { LabeledInput },
  data() {
    return {
      inputValue: 50,
    };
  },
};
</script>
