<template>
    <div class="relative h-96 bg-yellow-100">
        <div class="absolute mb-4 bottom-0 inset-x-0 z-10">
                <ol class="flex justify-center">
                    <li v-for="(image, i) in images" :key="i"
                        class="w-4 h-4 rounded-full cursor-pointer mx-2" :class="active === i ? 'bg-gray-300' : 'bg-gray-500'" @click="active=i"></li>
                </ol>
            </div>
        <div class="h-full bg-yellow-100">
            <a v-for="(image, i) in images" :key="i" :class="imagePositionClass(i)" :href="image.link" class="absolute flex justify-center h-full w-full ease-in-out transition-all duration-700">
                <img :src="image.src" />
            </a>
        </div>
    </div>
</template>

<script>
export default {

    props: {
        images: Array,
        startAt: {
            Type: Number,
            default: 0
        }
    },

    created() {
        this.active = this.startAt
    },

    methods: {
        imagePositionClass(i) {
            if (i < this.active)
                return "-left-full hidden"
            else if (i > this.active)
                return "-right-full hidden"
        }
    }
}
</script>
