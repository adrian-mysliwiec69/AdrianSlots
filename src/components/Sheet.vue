<template>
  <div class="slot-style">
    <button v-on="$listeners"><slot /></button>
  </div>
</template>

<style lang="scss" scoped></style>
<style scoped>
.slot-style {
  padding: 15px;
  width: 300px;
  height: 300px;
  box-shadow: 0 3px 5px -1px rgba(0, 0, 0, 0.2),
    0 6px 10px 0 rgba(0, 0, 0, 0.14), 0 1px 18px 0 rgba(0, 0, 0, 0.12);
}
</style>
