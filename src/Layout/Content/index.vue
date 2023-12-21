<template>
    <div class="wn-content">
        <!-- <div v-for="item in 100">{{ item }}</div> -->
        <table>
            <thead>
                <tr>
                    <th>文件名称</th>
                    <th>状态</th>
                    <th>信息</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item in 100">
                    <td>{{ item }}</td>
                    <td>18</td>
                    <td>男</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
@include b(content) {
    flex: 1;
    overflow: auto;
    // @include e(items) {
    //     padding: 1%;
    //     margin: 1%;
    //     border: 1px solid #ccc;
    //     border-radius: 4px;
    //     border-collapse: collapse;
    //     // 表格列自适应宽度
    //     table-layout: fixed;
    //     width: 98%;
    // }
}

table,
td {
    padding: 1%;
    margin: 1%;
    border: 1px solid #ccc;
    border-radius: 4px;
    border-collapse: collapse;
    // 表格列自适应宽度
    table-layout: fixed;
    width: 98%;
}
</style>
