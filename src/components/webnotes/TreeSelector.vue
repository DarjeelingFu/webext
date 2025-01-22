<script setup>

</script>

<template>
  <div id="TScontainer" class="flexRow">
    <div class="panel">
      tree
    </div>
  </div>
</template>

<style scope lang="scss">
@use '@assets/myCommon.scss';

$ctnShadowPadding: 5px;
#TScontainer {
  width: calc(100% - #{$ctnShadowPadding} * 2);
  height: calc(100% - #{$ctnShadowPadding} * 2);
}
</style>