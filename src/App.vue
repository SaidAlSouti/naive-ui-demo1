<template>
<n-space vertical size="large" :style="{padding: 24 + 'px'}">
  <hello-world></hello-world>
  <d-table></d-table>
</n-space>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import { NSpace } from 'naive-ui'
import DTable from './components/DTable.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    NSpace,
    DTable
    // NLayout
  }
}
</script>

<style>

</style>
