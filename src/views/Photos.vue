<template>
    <div>
        <h1>Photo Gallery</h1>

        <router-link
        :to="{ name: 'Photos', params: {id: item} }"
        v-for="(item, index) of picArr"
        :key="index"
         >
            <button>Pic {{ item }}</button>
        </router-link>
        <Pic />

        <button @click="home">Home</button>
        <button @click="back">Back</button>
        <button @click="next">Next</button>
    </div>
</template>

<script>

import Pic from '@/components/Photo.vue';
export default {
    name: 'Photos',
    components: {
        Pic
    },
    data() {
        return {
            picArr: [1, 2, 3]
        }
    },
    methods: {
        home() {
            this.$router.push('/')
        },
        back() {
            this.$router.go(-1)
        },
        next() {
            this.$router.go(1)
        }
    }
}
</script>