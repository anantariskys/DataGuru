<script>
  import TentangImage from "../../assets/Ilustrasi_Tentang.png";
  import InfoCard from "../../components/InfoCard.svelte";
  import Ticker from "../../components/Ticker.svelte";

  const contentAbout = [
    "DataGuru merupakan sebuah platform pembelajaran daring yang menawarkan akses tak terbatas terhadap basis data yang luas dan beragam mengenai berbagai topik seputar database.",
    "Kami berkomitmen untuk menyediakan konten-konten berkualitas tinggi secara cuma-cuma dan dapat diakses secara online oleh siapa pun, kapanpun, dan di mana pun. Kami percaya bahwa pendidikan dan ilmu pengetahuan seharusnya terbuka bagi semua kalangan, tanpa terkecuali.",
    "Oleh karena itu, DataGuru berupaya untuk menjadi sumber pembelajaran yang lengkap, terpercaya, dan terdepan dalam menyajikan informasi terkini seputar dunia database dari berbagai sumber terpercaya",
  ];
</script>

<section class="flex h-screen items-center justify-between container">
  <img src={TentangImage} class="w-2/5" alt="Tentang" draggable="false" />
  <main class="space-y-3 w-2/4">
    <h3 class="text-2xl font-semibold">Tentang Kami</h3>
    <h1
      class="bg-gradient-to-r w-fit from-[#FDB397] to-[#FD1E69] bg-clip-text text-transparent text-5xl font-semibold"
    >
      DataGuru
    </h1>
    <article class="prose-sm text-sm">
      {#each contentAbout as item}
        <p>
          {item}
        </p>
      {/each}
    </article>
    <div class="flex justify-between">
      <InfoCard title="Didirikan" subtitle="Tanggal Didiri">
        <Ticker
          slot="value"
          end={2024}
          afterNumeric={" Juni"}
          duration={2000}
        />
      </InfoCard>
      <InfoCard title="Total Pengguna" subtitle="Jumlah Pengguna">
        <Ticker slot="value" end={100000} duration={2000} />
      </InfoCard>
      <InfoCard title="Developers" subtitle="Jumlah Developer">
        <Ticker slot="value" end={6} duration={2000} afterNumeric={""} />
      </InfoCard>
    </div>
  </main>
</section>
