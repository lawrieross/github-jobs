<template>
  <div class="location">
    <h3 class="title">
      Location
    </h3>
    <form action="" class="search">
      <Public />
      <input
        type="text"
        placeholder="City, state, zip code or country"
      />
    </form>
    <div class="selection-container">
      <label for="location" class="selection">
        <input type="radio" name="location">
        London
      </label>
      <label for="location" class="selection">
        <input type="radio" name="location">
        Amsterdam
      </label>
      <label for="location" class="selection">
        <input type="radio" name="location">
        New York
      </label>
      <label for="location" class="selection">
        <input type="radio" name="location">
        Berlin
      </label>
    </div>
  </div>
</template>

<script>
import Public from '../icons/Public'

export default {
  name: 'Location',
  components: { Public }
}
</script>

<style lang="less" scoped>
@import '~@/assets/less/variables.less';

.location {
  .title {
    color: @faded-grey;
    font-family: 'Poppins';
    font-size: 14px;
    text-transform: uppercase;
    margin-bottom: 14px;
  }
  .search {
    display: flex;
    align-items: stretch;

    padding: 16px;
    margin-bottom: 24px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.05);
    min-height: 50px;
    background-color: #fff;
    border-radius: 4px;
    overflow: hidden;
    input {
      // Line clamp
      overflow: hidden;
      text-overflow: ellipsis;
      white-space: nowrap;

      font-size: 12px;
      border: none;
      width: 100%;
      &:focus {
        outline: none;
      }
      &::placeholder {
        color: @faded-grey;
      }
    }
  }
  .selection {
    display: flex;
    align-items: center;

    color: @primary;
    font-family: 'Poppins';
    font-weight: 500;
    font-size: 14px;
    margin-bottom: 16px;
    &:last-child {
      margin-bottom: 0;
    }
    &-container {
      display: flex;
      flex-direction: column;
      input[type="radio"] {
        margin-right: 8px;
      }
    }
  }
}
</style>
