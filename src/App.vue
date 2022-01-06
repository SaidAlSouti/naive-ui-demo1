<template>
  <n-layout>
    <n-layout-header bordered="true">
      <n-menu v-model:value="activeKey" mode="horizontal" :options="menuOptions" />
    </n-layout-header>
    <n-layout-content content-style="padding: 24px;">
      <hello-world></hello-world>
      <d-table></d-table>
    </n-layout-content>
  </n-layout>
  <!-- <n-space vertical size="large" :style="{padding: 24 + 'px'}">
  <hello-world></hello-world>
  <d-table></d-table>
</n-space> -->
</template>

<script>
import { h, ref } from 'vue'
import HelloWorld from "./components/HelloWorld.vue";
import { NSpace, NLayout, NMenu } from "naive-ui";
import DTable from "./components/DTable.vue";

import { NIcon } from 'naive-ui'
import {
  BookOutline as BookIcon,
  PersonOutline as PersonIcon,
  WineOutline as WineIcon
} from '@vicons/ionicons5'

function renderIcon (icon) {
  return () => h(NIcon, null, { default: () => h(icon) })
}

const menuOptions = [
  {
    label: () =>
      h(
        'a',
        {
          href: 'https://en.wikipedia.org/wiki/Hear_the_Wind_Sing',
          target: '_blank',
          rel: 'noopenner noreferrer'
        },
        'Hear the Wind Sing'
      ),
    key: 'hear-the-wind-sing',
    icon: renderIcon(BookIcon)
  },
  {
    label: 'Pinball 1973',
    key: 'pinball-1973',
    icon: renderIcon(BookIcon),
    disabled: true,
    children: [
      {
        label: 'Rat',
        key: 'rat'
      }
    ]
  },
  {
    label: 'A Wild Sheep Chase',
    key: 'a-wild-sheep-chase',
    disabled: true,
    icon: renderIcon(BookIcon)
  },
  {
    label: 'Dance Dance Dance',
    key: 'Dance Dance Dance',
    icon: renderIcon(BookIcon),
    children: [
      {
        type: 'group',
        label: 'People',
        key: 'people',
        children: [
          {
            label: 'Narrator',
            key: 'narrator',
            icon: renderIcon(PersonIcon)
          },
          {
            label: 'Sheep Man',
            key: 'sheep-man',
            icon: renderIcon(PersonIcon)
          }
        ]
      },
      {
        label: 'Beverage',
        key: 'beverage',
        icon: renderIcon(WineIcon),
        children: [
          {
            label: 'Whisky',
            key: 'whisky'
          }
        ]
      },
      {
        label: 'Food',
        key: 'food',
        children: [
          {
            label: 'Sandwich',
            key: 'sandwich'
          }
        ]
      },
      {
        label: 'The past increases. The future recedes.',
        key: 'the-past-increases-the-future-recedes'
      }
    ]
  }
]
export default {
  name: "App",
  setup(){
    return{
      activeKey: ref(null),
      menuOptions
    }
  },
  components: {
    HelloWorld,
    NSpace,
    DTable,
    NLayout
  },
};
</script>

<style>
</style>
