<script>
    import Logo from './Logo.vue'
    import Book from './Book.vue'
    import data from '../data.json'
    export default {
        data() {
            return {
                data,
                bookStyle: 'w-full h-[224px]'
            }
        },
        components: {
            Logo,
            Book,
        },
        computed: {
            items() {
                return this.data.slice(0,4);
            }
        }
    }
</script>

<template>
    <div class="w-full h-[779px] flex justify-center">
        <div class="w-[90%] h-full">
            <div class="flex w-full h-[224px] mt-[15px]">
                <span class="w-[60%] text-8xl font-bold flex justify-center text-center items-center">Our Store</span>
                <div class="w-full flex items-center justify-center">
                    <Logo class="w-[15%] h-[220px]" url="https://pisces.bbystatic.com/image2/BestBuy_US/images/products/6505/6505727cv15d.jpg"></Logo>
                    <Logo class="w-[15%] h-[220px] mx-[1.5%]" url="https://arystorephone.com/wp-content/uploads/2022/10/ipad-pro-11-2022-gray-2.jpg"></Logo>
                    <Logo class="w-[15%] h-[220px]" url="https://store.storeimages.cdn-apple.com/8756/as-images.apple.com/is/MPU73_AV3?wid=1144&hei=1144&fmt=jpeg&qlt=90&.v=1678830615848"></Logo>
                    <Logo class="w-[15%] h-[220px] mx-[1.5%]" url="https://image.oppo.com/content/dam/oppo/common/mkt/v2-2/reno6-pro-5g-oversea/navigation/Homepage-header2-Grey-427-x-600.png.thumb.webp"></Logo>
                    <Logo class="w-[15%] h-[220px]" url="https://www.notebookcheck.net/uploads/tx_nbc2/SamsungGalaxyA32.jpg"></Logo>
                </div>
            </div>
            <div class="w-full text-[40px] font-bold text-center mt-[15px]">
                <span>Best Sell</span>
            </div>
            <div class="w-full flex h-[286px] items-center justify-between px-[2%] mt-[20px]">
                <div v-for="item in items" :key="item.id" class="h-full bg-slate-300">
                    <RouterLink :to="{name: 'product', query: {id: item.id}}">
                        <Book class="h-full"
                            :url="item.url"
                            :title="item.title"
                            :price="(item.price).toFixed(2)"
                            :style="bookStyle">
                        </Book>
                    </RouterLink>
                </div>
            </div>
        </div>
    </div>
</template>