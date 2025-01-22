<script setup lang="ts">
import { Notivue, Notification } from 'notivue'
</script>

<template>
  <div>
    <div>
      <RouterView />
    </div>

    <Notivue v-slot="item">
      <Notification :item="item" />
    </Notivue>
  </div>
</template>

<style scoped></style>
