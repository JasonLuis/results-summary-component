<template>
  <div class="summary_reaction row items-center justify-between">
    <div class="row">
      <q-icon :name="`img: ${getImageToShow(props.icon)}`"></q-icon>
      <div class="summary-description" role="contentinfo">
        {{ props.description }}
      </div>
    </div>

    <div class="summary-score" role="contentinfo">
      {{ props.score }}<span> / 100</span>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  icon: string;
  description: string;
  score: number;
  color: string;
}>();

function getImageToShow(name: string) {
  const getImageUrl = new URL(`../../assets/icon/${name}`, import.meta.url)
    .href;

  return getImageUrl;
}

const color = computed(() => {
  return `var(${props.color})`;
});
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Hanken+Grotesk:wght@500;700&family=Heebo:wght@400;700&display=swap');

%text {
  font-family: 'Hanken Grotesk';
  font-style: normal;
}

.summary_reaction {
  width: 288px;
  height: 56px;
  border-radius: 12px;
  padding-left: 16px;
  padding-right: 10px;
  background: linear-gradient(
      0deg,
      rgba(255, 255, 255, 0.95),
      rgba(255, 255, 255, 0.95)
    ),
    v-bind(color);
  &:deep(.summary-description) {
    @extend %text;
    font-weight: 500;
    font-size: 18px;
    line-height: 23px;
    color: v-bind(color);
    padding-left: 12px;
  }
  &:deep(.summary-score) {
    @extend %text;
    padding-left: 81px;
    font-weight: 700;
    font-size: 18px;
    line-height: 23px;
    color: $dark;
  }
  &:deep(.summary-score span) {
    opacity: 0.5;
  }
  @media (max-width: $breakpoint-sm) {
    width: 100%;
  }
}

.q-icon {
  width: 20px;
  height: 20px;
}
</style>
