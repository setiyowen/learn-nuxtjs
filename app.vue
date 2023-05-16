<template>
  <NuxtLayout>
    <div class="bg-gray-100">
      <header class="bg-gray-900 py-4">
        <div class="container mx-auto flex justify-between items-center px-4">
          <h1 class="text-white text-3xl font-bold">Tutorial Membuat Kopi</h1>
          <nav>
            <ul class="flex text-white text-lg">
              <li class="mx-3">
                <a href="#pengenalan">Bahan dan cara membuat kopi</a>
              </li>
              <li class="mx-3"><a href="#video">Video membuat kopi</a></li>
            </ul>
          </nav>
        </div>
      </header>

      <main class="container mx-auto py-6 text-lg">
        <section id="pengenalan">
          <div>
            <h2 class="text-2xl font-bold mb-4">Bahan dan Cara Membuat Kopi</h2>
            <div class="section w-5"></div>
            <!-- <img
              class="w-auto h-10 rounded-xl"
              src="https://img.freepik.com/free-vector/coffee-love-foam-with-beans-cartoon-icon-illustration_138676-2575.jpg?w=2000"
              alt=""
            /> -->
            <div>
              <CoffeeCard
                v-for="coffee in coffees"
                :key="coffee.id"
                :title="coffee.title"
                :image="coffee.image"
                :altText="coffee.altText"
                :description="coffee.description"
              />
            </div>
          </div>
          <div class="flex flex-wrap">
            <div class="w-full lg:w-1/2 px-4 mb-6 lg:mb-0">
              <h3 class="text-lg font-bold mb-4">Bahan</h3>
              <ul class="list-disc list-inside">
                <li>Kopi 2 sdm</li>
                <li>Gula pasir 2 sdt, secukupnya</li>
                <li>Air Panas 150 ml</li>
              </ul>
            </div>
            <div class="w-full lg:w-1/2 px-4">
              <h3 class="text-lg font-bold mb-4">Cara Membuat Kopi</h3>
              <ol class="list-decimal list-inside">
                <li>Masukkan kopi sachet dan gula pasir ke dalam cangkir.</li>
                <li>Rebus air hingga mendidih</li>
                <li>
                  Jika sudah mendidih, Kemudian tuang kedalam cangkir yang sudah
                  berisi kopi dan gula. aduk hingga rata
                </li>
                <li>Sajikan kopi selagi masih hangat.</li>
              </ol>
            </div>
          </div>
          <p class="text-lg mt-6 flex-auto">
            Dengan minum kopi maka bisa mengurangi rasa lelah sehingga dapat
            menambah stamina atau energy. Hal ini disebabkan, kopi mengandung
            stimulan bernama kafein. <br />
            Jika diminum maka bisa mempengaruhi cara kerja otak dan menghasilkan
            efek rangsangan. Sehingga bisa meningkatkan level energy, kesadaran,
            suasana hati dan fungsi otak.
          </p>
        </section>

        <section id="video" class="mt-12">
          <h2 class="text-2xl font-bold mb-4">Video membuat kopi</h2>
          <div class="relative">
            <div class="flex justify-center mt-5">
              <div class="relative" style="height: 0; padding-bottom: 20%">
                <iframe
                  class="w-96 h-52 rounded-xl shadow-lg"
                  src="https://www.youtube.com/embed/GpTrxGDCDWA"
                  title="YouTube video"
                  allowfullscreen
                ></iframe>
              </div>
            </div>
          </div>
        </section>
        <footer class="w-full bg-gray-900 py-4">
          <div class="container mx-auto px-4 text-center text-sm">
            <p class="text-white">&copy; 2023 Website. cara membuat kopi.</p>
          </div>
        </footer>
      </main>
    </div>
  </NuxtLayout>
</template>
<script>
import CoffeeCard from "~/components/CoffeeCard.vue";

export default {
  components: {
    CoffeeCard,
  },
  data() {
    return {
      coffees: [
        {
          id: 1,
          title: "",
          image:
            "https://img.freepik.com/free-photo/cup-coffee-with-pile-coffee-beans_1112-438.jpg?size=626&ext=jpg&ga=GA1.2.815384605.1684142759&semt=sph",
          altText: "Kopi Hitam ",
          description:
            "Kopi Hitam nikmati secangkir kopi hitam yang pekat dengan aroma yang khas.",
        },
      ],
    };
  },
};
</script>
