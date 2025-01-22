<script setup>

</script>

<template>
  <div id="NUcontainer" class="flexRow">
    <div class="panel">
      upload
    </div>
  </div>
</template>

<style scope lang="scss">
@use '@assets/myCommon.scss';

$ctnShadowPadding: 5px;
#NUcontainer {
  width: calc(100% - #{$ctnShadowPadding} * 2);
  height: calc(100% - #{$ctnShadowPadding} * 2);
}
</style>