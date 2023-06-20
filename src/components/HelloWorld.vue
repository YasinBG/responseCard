<template>
  <section class="container md:flex md:justify-center">
  <div v-for="kisi in kisiler" :key="kisi" class="flex flex-col px-2  md:flex rounded-sm  bg-gray-200  my-4 md:w-1/4 mx-4 ">
    <div class="h-1/2">
      <img :src="kisi.resim" alt="" class="w-full object-cover container h-full">

    </div>
    <div class="flex flex-col  justify-center w-1/2 my-6 mx-auto items-center p-2">
      <h1 class="text-center text-2xl font-semibold text-blue-700 uppercase">{{ kisi.ad }}</h1>
      <p class="text-center mt-2 font-semibold">Yasi:{{ kisi.yas }}</p>
      <p class="mt-2 font-semibold uppercase ">Karakteri: {{ kisi.karakter }}</p>
      <P class="mt-2">{{ kisi.bilgi }}</P>
      
      <button class="bg-green-400 font-semibold rounded-xl w-36 h-10 mt-4      mx-auto justify-items-center mb-4 md:mb-0 px-2">DETAYLI BILGI</button>
    </div>

  </div>
</section>
</template>

<script>
import { ref } from 'vue'
export default {
  name:'HelloWorld',
  components:{

  },
  setup() {
    let kisiler =ref([{
      ad:"kral sakir",
      yas:"8",
      karakter:"aslan",
      resim:"https://st2.myideasoft.com/shop/bn/17/myassets/products/594/kral-sakir-23-cm-karton-tabak-8-adet-16550.jpeg?revision=1679507733",
      bilgi:"Şakir: Dizideki baş kahramandır. Bir aslandır ve sürekli olarak şapka takar. · Remzi: Şakir ve Canan'ın babası, Kadriye'nin eşidir. Bir aslandır."

    },
    {
      ad:"canan",
      yas:"10",
      karakter:"kedi",
      resim:"https://i.pinimg.com/originals/82/3b/e1/823be13b1654a49b817369aaf69f8d50.jpg",
      bilgi:"Canan: Beyaz renkli bir kedidir. Şakir'in kız kardeşidir. Çok akıllıdır ve genelde kitap okur. Bazı bölümlerde Şakir, Remzi ve Necati'yle maceraya atılır."
    },
    {
      ad:"necati",
      yas:"15",
      karakter:"fil",
      resim:"https://i.pinimg.com/originals/5f/f2/29/5ff22937290b96d888de508e22f4e302.png",
      bilgi:"Fil Necati: Mor renkli bir fildir. Anne ve babası zengin olsa da, kendisi zengin değildir. Okulda hademelik yapar. Geri kalan saatlerinde uyur, yemek yer ve video oyunu oynar. Genelde hep aylak aylak dolaşır. Remzi'nin en iyi arkadaşıdır. Birbirlerinden asla ayrılmazlar."
    }
  ])
    return {
      kisiler

    }
  }

}
</script>

<style>

</style>