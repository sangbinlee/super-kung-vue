<template>
  <!-- <KVBtn
    class="block"
    icon="material-symbols:settings-rounded"
    @click="$router.push('/settings')"
  /> -->
  <div class="font-retro text-xs opacity-50">v.1</div>
  <KVBtn
    v-if="isGameInProgress"
    is-retro
    is-upper-case
    label="Reset Game"
    @click="resetGame('exit')"
  />
</template>

<script setup lang="ts">
import { usePlayerStore } from '~/store/player'

const { resetGame } = usePlayerStore()
const { isGameInProgress } = storeToRefs(usePlayerStore())
</script>

<style scoped></style>
