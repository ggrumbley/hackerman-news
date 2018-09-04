<template>
  <div class="table-row">
    <span class="large-column">
      <a href="#">title</a>
    </span>
    <span class="mid-column">author</span>
    <span class="small-column">comments</span>
    <span class="small-column">points</span>
    <span class="small-column">
      <button class="button-inline">Dismiss</button>
    </span>
  </div>
</template>

<script>
export default {
  name: 'Table',
};
</script>


<style lang="scss" scoped>
  .table {
    margin: 20px 0;
  }
  .table-header {
    display: flex;
    line-height: 24px;
    font-size: 16px;
    padding: 0 10px;
    justify-content: space-between;

    > span {
      overflow: hidden;
      text-overflow: ellipsis;
      padding: 0 5px;
    }
  }
  .table-empty {
    margin: 200px;
    text-align: center;
    font-size: 16px;
  }
  .table-row {
    display: flex;
    line-height: 24px;
    white-space: nowrap;
    margin: 10px 0;
    padding: 10px;
    background: #ffffff;
    border: 1px solid #e3e3e3;

    > span {
      overflow: hidden;
      text-overflow: ellipsis;
      padding: 0 5px;
    }
  }
  .large-column {
    width: 40%;
  }
  .mid-column {
    width: 30%;
  }
  .small-column {
    width: 10%;
  }
</style>
