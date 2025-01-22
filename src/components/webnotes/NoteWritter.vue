<script setup>
import Textarea from 'primevue/textarea';
import Vditor from 'vditor'
import 'vditor/dist/index.css';

let value = ref('');
const vditor = ref()

onMounted(() => {
  // vditor.value = new Vditor('vditor',{
  //   height: '100%',
  //   width: '100%',
  //   lang: 'en_US',
  // })
})
</script>

<template>
  <div id="NWcontainer" class="flexRow">
    <div class="panel">
      editor
      <div id="vditor"></div>
    </div>
  </div>
</template>

<style scope lang="scss">
@use '@assets/myCommon.scss';

$ctnShadowPadding: 5px;

#NWcontainer {
  width: calc(100% - #{$ctnShadowPadding} * 2);
  height: calc(100% - #{$ctnShadowPadding} * 2);
}
</style>