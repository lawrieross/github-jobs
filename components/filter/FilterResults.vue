<template>
  <section class="filter-results">
    <label class="full-time" for="full-time">
      <input type="checkbox">
      Full time
    </label>
    <Location />
  </section>
</template>

<script>
import Location from './Location'

export default {
  name: 'FilterResults',
  components: { Location }
}
</script>

<style lang="less" scoped>
@import '~@/assets/less/variables.less';

.filter-results {
  input[type="checkbox"] {
    margin-right: 8px;
  }
  .full-time {
    display: flex;
    align-items: center;

    color: @primary;
    font-family: 'Poppins';
    font-size: 14px;
    font-weight: 500;
    margin-bottom: 32px;
  }
}
</style>
