<template>
  <label :for="lowerInputLabel">
    {{ inputLabel }}
    <input
      @input="updateValue"
      :value="value"
      :name="lowerInputLabel"
      :type="inputType"
      :min="min"
      :max="max"
    />
  </label>
</template>

<script>
export default {
  name: 'LabeledInput',
  props: [
    'inputLabel',
    'inputType',
    'value',
    'min',
    'max',
  ],
  methods: {
    updateValue(event) {
      this.$emit('input', event.target.value);
    },
  },
  computed: {
    lowerInputLabel() {
      return this.inputLabel.toLowerCase();
    },
  },
};
</script>
