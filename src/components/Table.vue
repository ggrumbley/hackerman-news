<template>
  <div class="table">
    <div class="table-header flex-row space-between">
      <span class="flex-4">Title</span>
      <span class="flex-2">Author</span>
      <span class="flex-1">Comments</span>
      <span class="flex-1">Points</span>
      <span class="flex-1">Archive</span>
    </div>
    <div class="table-row flex-row"
         v-for="(item, i) in list"
         :key="i">
      <span class="flex-4"><a :href="item.url">{{item.title}}</a></span>
      <span class="flex-3">{{item.author}}</span>
      <span class="flex-1">{{item.num_comments}}</span>
      <span class="flex-1">{{item.points}}</span>
      <span class="flex-1"><button class="button-inline">Dismiss</button></span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Table',
  computed: {
    list() {
      return this.$store.state.placeholderData;
    },
  },
};
</script>


<style lang="scss">
  @import "./../styles/vars";

  .table {
    margin: 20px 0;
  }
  .table-header {
    line-height: 24px;
    font-size: 16px;
    padding: 0 10px;

    > span {
      overflow: hidden;
      text-overflow: ellipsis;
      color: $chrome;
      font-family: 'Orbitron', sans-serif;
      font-size: 20px;
      font-weight: 1000;
      line-height: 1.2;
      text-transform: uppercase;
      background: -webkit-linear-gradient(top, #151C60, #C6CBF5 40%, black 40%, #E1A0CE 65%, white);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      -webkit-text-stroke-width: 1px;
      -webkit-text-stroke-color: white;
    }
  }
  .table-empty {
    margin: 200px;
    text-align: center;
    font-size: 16px;
  }
  .table-row {
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
</style>
