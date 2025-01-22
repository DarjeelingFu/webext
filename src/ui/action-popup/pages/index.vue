<script setup lang="ts">
import { ref, onMounted } from 'vue'
import TagSelector from '@/components/webnotes/TagSelector.vue';
import NotesWritter from '@/components/webnotes/NoteWritter.vue';
import NoteUploader from '@/components/webnotes/NoteUploader.vue';
import TreeSelector from '@/components/webnotes/TreeSelector.vue';

const openSidePanel = () => {
  chrome.runtime.sendMessage({ action: 'openSidePanel' })
}

</script>

<template>
  <div id="container" class="flexCol">
    <div id="infoArea" class="flexRow">
      <div id="tree" class="flexRow"><TreeSelector /></div>
      <div id="left" class="flexCol">
        <div id="tags" class="flexRow"><TagSelector /></div>
        <div id="notes" class="flexRow"><NotesWritter /></div>
      </div>
    </div>
    <div id="actionArea" class="flexRow"><NoteUploader /></div>
  </div>
</template>

<style scoped lang="scss">
@use '@assets/myCommon.scss';

$infoAreaHeightRatio: 0.7;
$leftWidthRatio: 0.55;
$tagsHeightRatio: 0.5;

#container {
  width: 500px;
  height: 500px;
  background-color: rgb(245, 245, 245);
}

#infoArea {
  width: 100%;
  height: calc(100% * #{$infoAreaHeightRatio});
}

#left {
  width: calc(100% * #{$leftWidthRatio});
  height: 100%;
}

#tags {
  width: 100%;
  height: calc(100% * #{$tagsHeightRatio});
}

#notes {
  width: 100%;
  height: calc(100% * (1 - #{$tagsHeightRatio}));
}

#tree {
  width: calc(100% * (1 - #{$leftWidthRatio}));
  height: 100%;
}

#actionArea {
  width: 100%;
  height: calc(100% * (1 - #{$infoAreaHeightRatio}));
}
</style>
