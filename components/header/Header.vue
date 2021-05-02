<template>
  <header class="header">
    <h1 class="title">
      <span class="bold">Github</span> Jobs
    </h1>
    <Search />
  </header>
</template>

<script>
import Search from './Search'

export default {
  name: 'Header',
  components: { Search }
}
</script>

<style lang="less" scoped>
@import '~@/assets/less/variables.less';
.header {
  margin-bottom: 24px;
  .title {
    color: @primary-heading;
    line-height: 36px;
    font-family: 'Poppins';
    font-size: 24px;
    font-weight: 300;
    margin: 0 0 32px;
    .bold { font-weight: 700; }
  }
}
</style>
