<template>
    <div class="flex flex-col justify-center items-center">
        <div class="relative flex flex-col items-center rounded-[20px] mx-auto p-4  bg-clip-border shadow-shadow-500  ">
            <div class="mt-6 mb-3 flex gap-14 md:!gap-14">
                <div class="pt-12 pr-0 pb-12 pl-0 mt-0 mr-auto mb-0 ml-auto sm:py-16 lg:py-20">
                    <div class="pt-0 pr-4 pb-0 pl-4 mt-0 mr-auto mb-0 ml-auto max-w-7xl sm:px-6 lg:px-8">
                        <div class="pt-0 pr-4 pb-0 pl-4 mt-0 mr-auto mb-0 ml-auto max-w-4xl sm:px-6 lg:px-8">
                            <div class="mt-8 mr-0 mb-0 ml-0 pt-4 pr-10 pb-4 pl-10 flow-root rounded-lg sm:py-2">
                                <div class="pt--10 pr-0 pb-10 pl-0">
                                    <a :href="item.href" class="cursor-pointer">
                                        <div
                                            class="bg-white rounded-xl pt-2 pr-5 pb-2 pl-5 mt-5 mr-0 mb-0 ml-0 shadow-xl hover:bg-violet-500 transition ease-in duration-500">
                                            <div class=" sm:flex sm:items-center sm:justify-between sm:space-x-5">
                                                <div class="flex items-center flex-1 min-w-0">
                                                    <img :src="item.img"
                                                        class="flex-shrink-0 object-cover rounded-full btn- w-10 h-10" />
                                                    <div class="mt-0 mr-0 mb-0 ml-4 flex-1 min-w-0">
                                                        <p class="text-lg font-bold text-gray-800">{{ item.title }}</p>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['item']
}
</script>