<script>
  import MateriImage from "../../assets/Materi.png";
  import BlogImage from "../../assets/Blog.png";
  import ForumImage from "../../assets/Forum.png";
  import QuizImage from "../../assets/Quiz.png";
  import SertifImage from "../../assets/Sertifikat.png";
  import Icon from "@iconify/svelte";

  let active = "Materi";
  const changeActive = (newActive) => {
    active = newActive;
  };

  const KontenFitur = [
    {
      judul: "Materi",
      subJudul: "Berbagai Materi Tentang Database",
      isi: "Kami membagikan berbagai materi pembelajaran yang komprehensif dan terkini seputar database. Di platform kami, Anda akan menemukan kursus lengkap dan studi kasus yang memungkinkan Anda memperdalam pemahaman tentang konsep dasar hingga topik-topik lanjutan dalam perancangan, pengembangan, dan pengelolaan database. Kami menjamin akses ke sumber daya terpercaya dan mutakhir bagi siapa pun yang ingin mempelajari dunia database yang dinamis.",
      gambar: MateriImage,
    },
    {
      judul: "Quiz",
      subJudul: "Jelajahi Tantangan Database yang menarik",
      isi: "Kami menyediakan rangkaian pertanyaan yang disusun secara cermat, mulai dari konsep dasar hingga topik-topik lanjutan, sehingga Anda dapat mengukur sejauh mana Anda telah memahami materi-materi penting ini. Tidak hanya itu, kuis kami juga memberikan kesempatan untuk mempraktikkan pengetahuan Anda melalui studi kasus yang relevan dan situasional.",
      gambar: QuizImage,
    },
    {
      judul: "Blog",
      subJudul: "Seputar Artikel Tentang Database",
      isi: "Dengan konten-konten yang terus diperbarui secara berkala, kami memastikan Anda tetap terhubung dengan tren terbaru dan praktik terbaik dalam dunia database yang terus berkembang. Artikel-artikel kami disusun secara hati-hati untuk memberikan wawasan yang mendalam namun mudah dipahami, sehingga siapa pun, dari pemula hingga ahli, dapat memperoleh manfaat dari kunjungan mereka ke halaman Blog kami.",
      gambar: BlogImage,
    },
    {
      judul: "Sertifikat",
      subJudul: "Tingkatkan Kredibilitas dan Peluang Karir Anda",
      isi: "Sertifikat yang kami berikan merupakan bukti konkret atas pencapaian Anda dan merupakan aset berharga dalam menunjukkan kompetensi Anda kepada dunia. Dibuat dengan cermat dan valid, sertifikat ini merupakan simbol keberhasilan Anda dalam menghadapi tantangan-tantangan dalam domain database.",
      gambar: SertifImage,
    },
    {
      judul: "Forum",
      subJudul: "Mulailah Berinteraksi",
      isi: "Forum kami menyediakan platform yang ideal bagi Anda untuk terhubung dengan sesama penggiat database, bertukar ide, dan memecahkan masalah bersama-sama. Apakah Anda seorang pemula yang mencari bimbingan, seorang profesional yang ingin berbagi pengalaman, atau seorang ahli yang ingin berdiskusi tentang topik-topik lanjutan, Forum kami memiliki tempat bagi Anda.",
      gambar: ForumImage,
    },
  ];

  const ListFitur = [
    {
      nama: "Materi",
      icon: "lets-icons:materials",
    },
    {
      nama: "Quiz",
      icon: "material-symbols:quiz",
    },
    {
      nama: "Blog",
      icon: "mdi:blog",
    },
    {
      nama: "Sertifikat",
      icon: "mdi:certificate",
    },
    {
      nama: "Forum",
      icon: "material-symbols:forum",
    },
  ];

  $: activeContent = () => {
    return KontenFitur.find((item) => item.judul === active);
  };


</script>

<section class="">
  <div class="flex justify-center gap-8 container">
    {#each ListFitur as item}
      <button
        on:click={() => changeActive(item.nama)}
        class={`flex rounded-t-lg gap-2 items-center py-2 font-semibold ${active === item.nama ? "bg-[#F6F5FF]" : "bg-[#CFCDDF]"} transition-colors duration-500 px-4`}
      >
        <Icon icon={item.icon} class="bg-white text-2xl p-1 rounded-sm" />
        {item.nama}
      </button>
    {/each}
  </div>
  <main class="bg-[#F6F5FF] py-10 flex items-center container justify-between">
    <div class="w-3/5 p-8">
      <h3 class="text-3xl font-semibold">{activeContent().judul}</h3>
      <h4 class="text-xl text-gray-500">{activeContent().subJudul}</h4>
      <p class="mt-4">{activeContent().isi}</p>
    </div>
    <img
      src={activeContent().gambar}
      alt={activeContent().judul}
      draggable="false"
      class="w-1/3"
    />
  </main>
</section>
