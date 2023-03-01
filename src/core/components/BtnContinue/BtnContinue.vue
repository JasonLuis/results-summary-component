<template>
  <q-btn no-caps>Continue</q-btn>
</template>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Hanken+Grotesk:wght@700&family=Heebo:wght@400;700&display=swap');

%text-label {
  font-family: 'Hanken Grotesk';
  font-style: normal;
  font-weight: 700;
  font-size: 18px;
  line-height: 23px;
  text-align: right;
}

.q-btn {
  @extend %text-label;
  width: 288px;
  height: 56px;
  border-radius: 128px;
  background-color: #303b59;
  color: $white;
  &:hover {
    background: linear-gradient(
      180deg,
      #7755ff 0%,
      #6943ff 0.01%,
      #2f2ce9 100%
    );
  }
}
</style>
