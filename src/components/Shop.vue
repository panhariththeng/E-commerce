<script>
    import { RouterLink } from 'vue-router'
    import Cate from './CateBook.vue'

    export default {
        data() {
            return {
                dim: 'w-[204px] h-[204px]'
            }
        },  
        components: {
            Cate,
        }
    }
</script>

<template>
    <div class="w-full h-[779px] flex justify-center">
        <div class="w-[90%] h-auto ">
            <div class="w-full flex items-center text-[1.125em] my-[55px]">
                <RouterLink to="/" class="hover:opacity-50">Home</RouterLink>
                &nbsp;>&nbsp;
                <RouterLink to="/shop" class="hover:opacity-50">Shop</RouterLink>
            </div>
            <div class="w-full flex items-center text-[2em]">
                <span>Categories</span>
            </div>
            <Cate class="mt-[23px]"
                genre="Best Window"
                :style="dim"
                url="https://www.cnet.com/a/img/resize/667c566e765f591431dedae84691194f08c57cde/hub/2020/01/02/145a13ff-fc7a-4015-a42b-fa91bd93a1ec/05-dell-xps-13.jpg?auto=webp&fit=crop&height=1200&width=1200"
                desc="Dell XPS (eXtreme Performance System) is a line of consumer-oriented high-end laptop and desktop computers manufactured by Dell. ">
            </Cate>
            <Cate class="mt-[21px]"
                genre="Best Phone"
                :style="dim"
                url="data:image/jpeg;base64,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"
                desc="The Galaxy Fold contains two displays; its front cover contains a small, 4.6-inch display in the center designed for one-handed use, and the device can fold">
            </Cate>
        </div>
    </div>
</template>