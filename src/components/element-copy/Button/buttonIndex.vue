<template>
  <div class="button-index">
   <!-- <button class="button fz-co" :class="type=== 'primary' ? 'bgpr' : type === 'success' ? 'bgsu' : type === 'info' ? 'bgif' : type === 'warning' ? 'bgwa' : type === 'danger' ? 'bgdg': ''">你好</button> -->
   <button class="button fz-co" :class="{bgpr: type === 'primary', bgsu: type === 'info', bgif: type === 'info', bgwa: type === 'warning', bgdg: type === 'danger', bgsu: type === 'success', large: size === 'large', small: size === 'small', disable: disable, plain: plain}">
    <slot><span></span></slot>
   </button>
  </div>
</template>

<script lang="ts">
import {defineComponent, onMounted, toRefs} from 'vue'
export default defineComponent({
  props: {
    type: String,
    size: String,
    disable:{
      type: Boolean,
      default: false
    }
  },
  setup() {

    // const { type } = toRefs(props)

    // onMounted(() => {
    // })
    return{}
    
  },
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.button-index{
  .button{
    // background: #ccc;
    height: 32px;
    border-radius: 4px;
    padding: 8px 12px;
    line-height: 1;
    cursor: pointer;
    border: none;

  }
  .large{
    padding: 12px 19px;
  }
  .small{
    padding: 5px 11px
  }
  .disable,.bgwa{
    cursor: not-allowed;
    background: #f3d19e;
  }
  .plain, .bgdg{
    border: 1px solid #f89898;
    background: #fde2e2;
    color: #f89898;


  }
}

</style>
