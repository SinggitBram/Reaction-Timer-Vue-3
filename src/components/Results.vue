<template>
   <div>
      <p>Kecepatan reaksi kamu: {{ score }}</p>
      <p class="rank">{{ rank }}</p>
   </div>
</template>

<script>
export default {
   props: ["score"],
   data() {
      return {
         rank: null,
      };
   },
   mounted() {
      if (this.score < 300) {
         this.rank = "Wow Reflek Kamu Secepat Kilat!";
      } else if (this.score < 400) {
         this.rank = "Lumayan Cepat, Tapi Masih Bisa Ditingkatkan!";
      } else {
         this.rank = "Kamu Sedikit Lambat, Ayo Latihan Lagi!";
      }
   },
};
</script>

<style>
.rank {
   font-size: 1.4em;
   color: #0faf87;
   font-weight: bold;
}
</style>

