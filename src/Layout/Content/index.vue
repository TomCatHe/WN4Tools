<template>
    <div class="wn-content">
        <!-- <div v-for="item in 100">{{ item }}</div> -->
        <table>
            <thead>
                <tr>
                    <th width="200px">文件名称</th>
                    <th width="80px">状态</th>
                    <th width="300px">信息</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item in items">
                    <td>{{ item.fileName }}</td>
                    <td>{{ item.status }}</td>
                    <td>{{ item.msg }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script setup lang="ts">
import { Ref, reactive } from "vue";

// 声明一个接口，然后定一个对象
interface item {
    fileName: string;
    status: string;
    msg: string;
}

let items = reactive<item[]>([
    {
        fileName: "usp_ghdj.sql",
        status: "未执行",
        msg: "",
    },
    {
        fileName: "usp_ghdj_ex.sql",
        status: "执行成功",
        msg: "",
    },
    {
        fileName: "usp_CDRGH001.sql",
        status: "未执行",
        msg: "",
    },
    {
        fileName: "usp_CDRGH003.sql",
        status: "执行失败",
        msg: "截断字符串",
    },
]);
</script>

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
    // table-layout: fixed;
    // width: 98%;
}
</style>
