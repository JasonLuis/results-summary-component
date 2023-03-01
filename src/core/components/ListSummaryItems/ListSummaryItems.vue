<template>
  <div class="list-summary">
    <UiSummaryItem
      icon="icon-reaction.svg"
      description="Reaction"
      :score="80"
      color="--q-secondary"
    />

    <UiSummaryItem
      class="q-mt-md"
      icon="icon-memory.svg"
      description="Memory"
      :score="92"
      color="--q-accent"
    />

    <UiSummaryItem
      class="q-mt-md"
      icon="icon-verbal.svg"
      description="Verbal"
      :score="61"
      color="--q-positive"
    />

    <UiSummaryItem
      class="q-mt-md"
      icon="icon-visual.svg"
      description="Visual"
      :score="73"
      color="--q-primary"
    />
  </div>
</template>

<script setup lang="ts">
import UiSummaryItem from '../SummaryItem/SummaryItem.vue';
</script>

<style scoped lang="scss">
.list-summary {
  height: 272px;
}
</style>
