<script>
export default {
    data() {
        return {
            seatRows: 16,
            seatColumns: 15,
        }
    },
    async mounted() {

    },
    beforeUnmount() {

    },
    methods: {

    }
}
</script>

<template>
    <div class="flex flex-col justify-center items-center w-vw-full h-1 min-h-screen bg-ui-background">
        <div class="flex flex-col justify-center items-center basis-11/12 h-full w-full">
            <div v-for="row in seatRows" class="flex w-full h-full justify-around items-center">
                <div v-for="column in seatColumns" class="bg-ui-card ring-ui-ring ring-1 w-8 h-8">

                </div>
            </div>
        </div>

        <div class="flex justify-center items-center basis-1/12 h-full w-full bg-ui-background">
            <div class="flex w-full h-full justify-center items-center">
                <button class="px-8 py-3 bg-ui-card rounded-lg ring-ui-ring ring-1">
                    <h1 class="text-white">asd</h1>
                </button>
            </div>

            <div class="flex w-full h-full justify-center items-center">
                <button class="px-8 py-3 bg-ui-card rounded-lg ring-ui-ring ring-1">
                    <h1 class="text-white">asd</h1>
                </button>
            </div>

            <div class="flex w-full h-full justify-center items-center">
                <button class="px-8 py-3 bg-ui-card rounded-lg ring-ui-ring ring-1">
                    <h1 class="text-white">asd</h1>
                </button>
            </div>
        </div>
    </div>
</template>
