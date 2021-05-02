<template>
  <div class="container">
    <Header />
    <main>
      <FilterResults />
      <JobListings />
    </main>
  </div>
</template>

<script>
import FilterResults from '../components/filter/FilterResults'
import Header from '../components/header/Header'

export default {
  components: { FilterResults, Header }
}
</script>

<style lang="less" scoped>
@import '~@/assets/less/variables.less';

.container {
  margin: 0 auto;
  font-family: 'Roboto';
  max-width: 1200px;
  padding: 12px;
  main {
    display: grid;
    grid-template-columns: 1fr;
  }
}

@media (min-width: 900px) {
  .container {
    padding: 32px 12px;
    main {
      column-gap: 32px;
      grid-template-columns: 1fr 2fr;
    }
  }
}
</style>
