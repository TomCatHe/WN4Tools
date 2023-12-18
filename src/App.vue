<template>
    <div id="container">
        <div id="filelist">文件列表</div>
        <div>
            <table width="600">
                <thead>
                    <tr>
                        <th>文件</th>
                        <th>状态</th>
                        <th>操作</th>
                    </tr>
                </thead>
                <tbody v-for="item in dataList">
                    <tr>
                        <td>{{ item.name }}</td>
                        <td>{{ item.status }}</td>
                        <td><button>Del</button></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>

<script setup lang="ts">
import { reactive } from "vue";

interface FileData {
    name: string;
    status: string;
    operation: string;
}

let dataList = reactive<FileData[]>([
    {
        name: "a.sql",
        status: "read",
        operation: "Del",
    },
    {
        name: "b.sql",
        status: "read",
        operation: "Del",
    },
    {
        name: "c.sql",
        status: "read",
        operation: "Del",
    },
]);
</script>

<style scoped>
* {
    padding: 0%;
    margin: 0%;
}

#container {
    height: 100%;
    width: 100%;
    overflow: hidden;
    /* background-color: #ccc; */
}

#filelist {
    height:200px;
    width:100px;
    float: left;
}

table {
    border: 1px solid #000;
    border-collapse: collapse;
    width:"600px";
}

th,
td {
    border: 1px solid #000;
    padding: 5px;
}

th {
    background-color: #ccc;
}

td {
    background-color: #eee;
}
</style>
