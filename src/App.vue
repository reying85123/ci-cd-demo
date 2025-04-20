<script setup>
import { ref } from 'vue'
import TestView from './components/TestView.vue'

const testString = ref('CI/CD Test')
</script>

<template>
  <TestView :msg="testString" />
</template>
