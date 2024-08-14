<script>
  import Fitur from "../sections/landingPage/Fitur.svelte";
  import Hero from "../sections/landingPage/Hero.svelte";
  import Tentang from "../sections/landingPage/Tentang.svelte";
  import Ulasan from "../sections/landingPage/Ulasan.svelte";
  
</script>

<svelte:head>
  <title>Beranda</title>
  <meta name="description" content="Ini adalah beranda" />
  <meta property="og:title" content="beranda" />
</svelte:head>

<Hero />
<Tentang />
<Fitur />
<Ulasan/>
