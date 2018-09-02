<template>
<div class="page">
  <div class="interactions">
    <Search />
  </div>
  <Table />
  <div class="interactions">
    <Button />
  </div>
</div>
</template>

<script>

import HelloWorld from '@/components/HelloWorld.vue';
import Button from '@/components/Button.vue';
import Search from '@/components/Search.vue';
import Table from '@/components/Table.vue';

export default {
  name: 'home',
  components: {
    HelloWorld,
    Button,
    Search,
    Table,
  },
};
</script>

<style lang="scss" scoped>
  .page {
    margin: 20px;
  }
  .interactions {
    text-align: center;
  }
  .table {
    margin: 20px 0;
  }
  .table-header {
    display: flex;
    line-height: 24px;
    font-size: 16px;
    padding: 0 10px;
    justify-content: space-between;
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
  }
  .table-header > span {
    overflow: hidden;
    text-overflow: ellipsis;
    padding: 0 5px;
  }
  .table-row > span {
    overflow: hidden;
    text-overflow: ellipsis;
    padding: 0 5px;
  }
  .button-inline {
    border-width: 0;
    background: transparent;
    color: inherit;
    text-align: inherit;
    -webkit-font-smoothing: inherit;
    padding: 0;
    font-size: inherit;
    cursor: pointer;
  }
  .button-active {
    border-radius: 0;
    border-bottom: 1px solid #38BB6C;
  }
</style>

