<script>
      import HeroImage from "../../assets/Ilustrasi_hero.png";
      import Button from "../../components/Button.svelte";
</script>

<section class="h-screen flex items-center justify-between container">
    <main class="space-y-4">
      <h3 class="text-2xl font-semibold">Selamat Datang di DataGuru</h3>
      <h1 class="text-6xl font-semibold lg:w-5/6">Menjadi Database Enginner <span class="bg-gradient-to-r from-[#FDB397] to-[#FD1E69] bg-clip-text text-transparent">Professional</span></h1>
      <p class="text-2xl lg:w-[89%]">Tingkatkan Kecerdasan Data Anda Mulailah Petualangan dengan Basis Data!</p>
      <Button variant='primary'>Mulai Belajar</Button>
    </main>
    <img class="w-2/5 aspect-auto" draggable="false" src={HeroImage} alt="Hero"/>
  </section>