<script setup lang="ts">
import { toRefs } from 'vue'
import type { Participant } from '@/types'
const props = defineProps<{
  participant: Participant
  id: string
}>()
const { participant } = toRefs(props)
</script>

<template>
  <div v-if="participant">
      <h1>{{ participant.name }}</h1>
      <p>{{ participant.email }}</p>
  </div>
  <div v-else>
    <p>Loading Participant...</p>
  </div>
</template>
