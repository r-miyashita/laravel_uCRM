<script setup>
import { Link } from '@inertiajs/inertia-vue3';
import { ref} from 'vue';

const newTitle = ref('')
const newContent = ref('')
</script>
<template>
    Inertiaテスト<br><br>
    <a href="/">a tag</a><br>
    <Link href="/">link tag</Link><br>
    <Link :href="route('inertia.index')">名前付きルート</Link>
    <Link :href="route('inertia.show', {id: 1})">ルートパラメータのテスト</Link>

    <div class="mb-8">
        <input type="text" v-model="newTitle"><br>
        <input type="text" v-model="newContent">
        <Link as="button" method="POST" :href="route('inertia.store')"
            :data="{
                title: newTitle,
                content: newContent
            }"
        >データ保存</Link>
    </div>
</template>
