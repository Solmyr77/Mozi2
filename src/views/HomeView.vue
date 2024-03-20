<script>
export default {
  data() {
    return {
      activeMenuItem: "none",
      selectedMenu: "none",
    }
  },
  async mounted() {
    this.$refs.seatsOption.addEventListener("click", () => {
      this.$router.push("/seats");
    });

    this.$refs.seatsOption.addEventListener("mouseover", () => {
      this.activeMenuItem = "seatsOption";
    });

    this.$refs.seatsOption.addEventListener("mouseleave", () => {
      this.activeMenuItem = "none";
    });


    this.$refs.bookingOption.addEventListener("click", () => {
      this.$router.push("/booking");
    });

    this.$refs.bookingOption.addEventListener("mouseover", () => {
      this.activeMenuItem = "bookingOption";
    });

    this.$refs.bookingOption.addEventListener("mouseleave", () => {
      this.activeMenuItem = "none";
    });
  },
  methods: {
  }
}
</script>

<template>
  <!--Main-->
  <div class="flex flex-col w-vw-full h-1 min-h-screen bg-ui-background">

    <!--Header-->
    <div class="flex justify-center items-center w-full basis-1/12">
      <h1 class="text-white hover:text-gray-400 text-3xl dm-sans-bold cursor-pointer">Kandó mozi</h1>
    </div>
    <!--Header-->

    <!--Content-->
    <div class="flex justify-center items-center w-full basis-11/12">
      <div class="flex justify-around items-center w-full h-full basis-1/3 flex-grow">

        <!--View seats option-->
        <div class="basis-1/2 justify-center items-center flex">
          <div
            :class="{ 'ring-ui-primary ring-2': activeMenuItem == 'seatsOption', 'text-gray-400 ring-ui-ring ring-1': activeMenuItem != 'seatsOption' }"
            ref="seatsOption"
            class="p-4 flex flex-col justify-between items-start w-72 h-36 bg-ui-card rounded-xl cursor-pointer duration-150">
            <h2 class="mb-4 dm-sans-semibold text-white text-2xl pointer-events-none select-none">Ülések</h2>
            <p class="dm-sans-regular text-gray-400 pointer-events-none select-none">Itt tekintheti meg az eddig
              lefoglalt és az elérhető helyeket.</p>
          </div>
        </div>
        <!--View seats option-->

        <!--Booking option-->
        <div class="basis-1/2 justify-center items-center flex">
          <div ref="bookingOption"
            :class="{ 'ring-ui-primary ring-2': activeMenuItem == 'bookingOption', 'text-gray-400 ring-ui-ring ring-1 duration-150': activeMenuItem != 'bookingOption' }"
            class="p-4 flex flex-col justify-between items-start w-72 h-36 bg-ui-card rounded-xl cursor-pointer">
            <h2 class="mb-4 dm-sans-semibold text-white text-2xl pointer-events-none select-none">Foglalás</h2>
            <p class="dm-sans-regular text-gray-400 pointer-events-none select-none">Itt léphet be a menübe és kezdheti
              meg a foglalási folyamatot.</p>
          </div>
        </div>
        <!--Booking option-->

      </div>
    </div>
    <!--Content-->

  </div>
  <!--Main-->
</template>
