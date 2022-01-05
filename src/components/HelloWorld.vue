<template>
  <n-space size="large">
    <n-button strong secondary>Default</n-button>
    <n-button strong secondary type="tertiary">Tertiary</n-button>
    <n-button strong secondary type="primary">Primary</n-button>
    <n-button strong secondary type="info">Info</n-button>
    <n-button strong secondary type="success">Success</n-button>
    <n-button strong secondary type="warning">Warning</n-button>
    <n-button strong secondary type="error">Error</n-button>
    <n-button strong secondary round>Default</n-button>
    <n-button strong secondary round type="primary">Primary</n-button>
    <n-button strong secondary round type="info">Info</n-button>
    <n-button strong secondary round type="success">Success</n-button>
    <n-button strong secondary round type="warning">Warning</n-button>
    <n-button strong secondary round type="error">Error</n-button>
    <n-button strong secondary circle
      ><n-icon><cash-icon /></n-icon
    ></n-button>
    <n-button strong secondary circle type="primary"
      ><n-icon><cash-icon /></n-icon
    ></n-button>
    <n-button strong secondary circle type="info"
      ><n-icon><cash-icon /></n-icon
    ></n-button>
    <n-button strong secondary circle type="success"
      ><n-icon><cash-icon /></n-icon
    ></n-button>
    <n-button strong secondary circle type="warning"
      ><n-icon><cash-icon /></n-icon
    ></n-button>
    <n-button strong secondary circle type="error"
      ><n-icon><cash-icon /></n-icon
    ></n-button>
  </n-space>

  
</template>



<script>
import { CashOutline as CashIcon } from '@vicons/ionicons5'
import { NButton, NSpace, NIcon } from 'naive-ui'
export default {
  name: 'HelloWorld',
  components: {
    NButton,
    NSpace,
    NIcon,
    CashIcon
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
