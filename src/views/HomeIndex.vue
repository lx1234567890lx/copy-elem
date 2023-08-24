<template>
  <!-- <div>HOME</div> -->
  <Button type="primary" size="large">移动</Button>
  <Button type="danger" plain size="small">查看</Button>
  <Button type="info">编辑</Button>
  <Button type="warning" :disable="true">删除</Button>
  <Button type="success">重置</Button>
  <!-- <Button type="success"></Button> -->
  
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Button from '@/components/element-copy/Button/buttonIndex.vue'

export default defineComponent({
  components: {
    Button
  },
  setup() {
    return{}
    
  },
})
</script>
