<template>
    <div class="flex flex-col justify-center items-center">
        <div class="p-4">
            <div class="flex">
                <div>
                    <div v-for="service, index in services" :key="index" class="pb-4">
                        <a :href="service.href" class="cursor-pointer">
                            <div
                                class="bg-teal-100 rounded-xl pt-2 pr-5 pb-2 pl-5 mt-5 shadow-xl hover:bg-teal-600 transition ease-in duration-500">
                                <div class=" sm:flex sm:items-center sm:justify-between sm:space-x-5">
                                    <div class="flex items-center flex-1 min-w-0">
                                        <img :src="service.img"
                                            class="flex-shrink-0 object-cover rounded-xl btn- w-10 h-10" />
                                        <div class="mt-0 mr-0 mb-0 ml-4 flex-1 min-w-0">
                                            <p class="text-lg font-bold text-gray-800">{{ service.title }}</p>
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
</template>

<script>
export default {
    data() {
        return {
            services: '',
        }
    },
    mounted() {
        fetch('https://raw.githubusercontent.com/ThiagoRazor/thiago-tree/main/src/data/socials.json')
            .then(res => res.json())
            .then(res => this.services = res)
            .catch(e => console.log(e))
    },
}
</script>
