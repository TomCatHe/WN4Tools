<template>
    <div style="margin-top: 20px">
        <table border width="600" cellpadding="0" :cellspacing="0">
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
    }
]);
</script>

<style scoped></style>
