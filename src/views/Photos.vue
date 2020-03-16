<template>
    <div>
        <h1>Photo Gallery</h1>
        <Pic />
    </div>
</template>

<script>

import Pic from '@/components/Photo.vue';
export default {
    name: 'Photos',
    components: {
        Pic
    }
}
</script>