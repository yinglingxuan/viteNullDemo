<template>
  <div class="index">
    <a-table :data-source="tableInfo.dataSource" :columns="tableInfo.columns" />
    <p class="index-test">{{ test }}</p>
  </div>
</template>

<script lang="ts" setup>
  const tableInfo = reactive({
    dataSource: [],
    columns: [
      {
        title: '姓名',
        dataIndex: 'name',
        key: 'name'
      },
      {
        title: '年龄',
        dataIndex: 'age',
        key: 'age'
      },
      {
        title: '住址',
        dataIndex: 'address',
        key: 'address'
      }
    ]
  })

  const test = reactive(
    Object.fromEntries([
      ['foo', 'bar'],
      ['baz', 42]
    ])
  )
</script>

<style lang="less" scoped>
  .index {
    position: relative;

    &-test {
      width: 100px;
    }
  }
</style>
