<script setup>
import { ref } from 'vue'
import TestView from './components/TestView.vue'

const testString = ref('CI/CD First Test')
</script>

<template>
  <TestView :msg="testString" />
</template>
