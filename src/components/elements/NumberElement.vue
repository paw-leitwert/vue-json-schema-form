<template>
  <b-field :label="schema.title" :message="schema.description">
    <b-input type="number" :min="schema.minimum" :max="schema.maximum" :step="schema.type === 'number' ? 'any': '1'" :value="value" :disabled="schema.disabled" @input="$emit('input', Number($event))">
    </b-input>
  </b-field>
</template>

<script>
export default {
  name: 'NumberElement',
  props: [
    'schema',
    'value'
  ]
}
</script>
