<template>
<div class="page">
  <div class="interactions">
    <Search />
  </div>
  <Table />
  <div class="interactions">
    <button>More</button>
  </div>
</div>
</template>

<script>

import HelloWorld from '@/components/HelloWorld.vue';
import Search from '@/components/Search.vue';
import Table from '@/components/Table.vue';

export default {
  name: 'home',
  components: {
    HelloWorld,
    Search,
    Table,
  },
};
</script>

<style lang="scss">
  .page {
    margin: 20px;
  }
  .interactions {
    text-align: center;
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

