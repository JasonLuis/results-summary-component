<template>
  <q-card class="no-shadow q-pa-none">
    <q-card-section class="row q-pa-none">
      <div class="col-lg-6 col-xs-12 result q-pa-none column items-center">
        <div class="result-text text-center full-width">Your Result</div>
        <div
          class="column justify-center shadow-box text-center result__score shadow-14"
        >
          <div class="score__achieved">76</div>
          <span>of 100</span>
        </div>
        <div class="score-title">Great</div>
        <p class="score-description">
          Your performance exceed 65% of the people conducting the test here!
        </p>
      </div>
      <div class="col-lg-6 col-xs-12 summary column">
        <div class="summary-text text-start full-width">Summary</div>
        <ListSummary class="mt-medium" />

        <UiButton class="mt-large" />
      </div>
    </q-card-section>
  </q-card>
</template>

<script setup lang="ts">
import ListSummary from '../ListSummaryItems/ListSummaryItems.vue';
import UiButton from '../BtnContinue/BtnContinue.vue';
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Hanken+Grotesk:wght@500;700;800&family=Heebo:wght@400;700&display=swap');

%text {
  font-family: 'Hanken Grotesk';
  font-style: normal;
}

.q-card {
  width: 736px;

  border-radius: 32px;
  @media (max-width: $breakpoint-xs) {
    width: 100%;
  }
}
.mt-medium {
  margin-top: 28px;
}

.mt-large {
  margin-top: 41px;
}

.result {
  height: 512px;
  background: linear-gradient(180deg, #7755ff 0%, #6943ff 0.01%, #2f2ce9 100%);
  border-radius: 32px;
  @media (max-width: $breakpoint-xs) {
    border-radius: 0px 0px 32px 32px;
    height: 356px;
  }
  &:deep(.result-text) {
    @extend %text;
    font-weight: 700;
    font-size: 24px;
    line-height: 31px;
    color: #cac9ff;
    margin-top: 38px;
    @media (max-width: $breakpoint-xs) {
      margin-top: 24px;
      font-size: 18px;
    }
  }
  &:deep(.score-title) {
    @extend %text;
    margin-top: 28px;
    font-weight: 700;
    font-size: 32px;
    line-height: 42px;
    text-align: center;
    color: #ffffff;
    @media (max-width: $breakpoint-xs) {
      margin-top: 24px;
      font-size: 24px;
    }
  }
  &:deep(.score-description) {
    @extend %text;
    width: 260px;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 23px;
    text-align: center;
    color: #cac9ff;
    @media (max-width: $breakpoint-xs) {
      font-size: 16px;
    }
  }
}

.result__score {
  width: 200px;
  height: 200px;
  margin-top: 35px;
  border-radius: 100%;
  background: linear-gradient(
    180deg,
    #4d21c9 0%,
    rgba(37, 33, 201, 0) 100%,
    rgba(37, 33, 201, 0) 100%
  );
  @media (max-width: $breakpoint-xs) {
    width: 140px;
    height: 140px;
    margin-top: 24px;
    -webkit-box-shadow: none;
    -moz-box-shadow: none;
    box-shadow: none;
  }
}

.result__score {
  &:deep(.score__achieved) {
    @extend %text;
    font-weight: 800;
    font-size: 72px;
    text-align: center;
    color: #ffffff;
    line-height: 72px;
    @media (max-width: $breakpoint-xs) {
      font-size: 56px;
    }
  }
}

.result__score span {
  @extend %text;
  font-weight: 700;
  font-size: 18px;
  color: #cac9ff;
  mix-blend-mode: normal;
  opacity: 0.52;
  line-height: 23px;

  @media (max-width: $breakpoint-xs) {
    font-size: 16px;
  }
}
.summary {
  height: 512px;
  padding-top: 38px;
  padding-left: 40px;
  &:deep(.summary-text) {
    @extend %text;
    font-weight: 700;
    font-size: 24px;
    line-height: 31px;
    color: #303b59;
  }
  @media (max-width: $breakpoint-sm) {
    padding-left: 40px;
    padding-right: 40px;
  }
}
</style>
