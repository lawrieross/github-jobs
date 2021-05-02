<template>
  <section class="search-bar" :style="image">
    <form action="" class="search">
      <div class="input-text">
        <Briefcase />
        <input
          type="text"
          placeholder="Title, companies, expertise or benefits"
        />
      </div>
      <button class="search-button">
        Search
      </button>
    </form>
  </section>
</template>

<script>
import BgImage from '~/assets/images/backgroundImg.png'
import Briefcase from '../icons/Briefcase'

export default {
  name: 'Search',
  components: { Briefcase },
  data() {
    return {
      image: { backgroundImage: `url(${BgImage})` }
    }
  }
}
</script>

<style lang="less" scoped>
@import '~@/assets/less/variables.less';

.search-bar {
  border-radius: 8px;
  padding: 42px 18px;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  margin-bottom: 32px;
}
.search {
  position: relative;
  display: flex;
  align-items: stretch;
  justify-content: space-between;
  
  min-height: 50px;
  background-color: #fff;
  border-radius: 4px;
  overflow: hidden;
  padding: 4px;
  .input-text {
    display: flex;
    align-items: center;
    padding: 0 16px;
    width: 100%;
    input {
      // Line clamp
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;

      color: @faded-grey;
      font-size: 12px;
      line-height: 14px;
      border: none;
      height: 100%;
      width: 100%;
      padding: 0;
      &:focus {
        outline: none;
      }
      &::placeholder {
        color: @faded-grey;
      }
    }
  }
  &-button {
    display: flex;
    align-items: center;
    justify-content: center;

    font-weight: 500;
    font-size: 16px;
    line-height: 18.75px;
    padding: 0 24px;  
    color: #fff;
    background-color: @bg-search-button;
    border: none;
    border-radius: 4px;
  }
  #briefcase {
    fill: @faded-grey;
    margin-right: 10px;
  }
}
</style>
