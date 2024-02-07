<script setup>
import GestLayout from '@/Layouts/GuestLayout.vue'
import Label from '@/Components/InputLabel.vue'
import Input from '@/Components/TextInput.vue'

const emitTest = e => console.log(e)

</script>
<template>
    <GestLayout>
        <Label value="件名">TITLE</Label>
        <Input modelValue="初期値" @update:modelValue="emitTest"></Input>
    </GestLayout>
</template>
