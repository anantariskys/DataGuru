<script>
  import { onMount } from "svelte";
  import ReviewCard from "../../components/ReviewCard.svelte";

  const ulasan = [
    {
      content:
        "Situs ini benar-benar membantu saya memahami konsep database dengan cara yang mudah dipahami. Terima kasih!",
      author: "Sarah",
    },
    {
      content:
        "Penjelasan dan contoh-contoh yang diberikan sangat jelas dan relevan. Rekomendasi untuk pemula seperti saya.",
      author: "Amir Rahmadi",
    },
    {
      content:
        "Saya suka bagaimana situs ini dibuat dengan gaya yang menarik dan interaktif. Belajar jadi lebih menyenangkan!",
      author: "Emily Wong",
    },
    {
      content:
        "Materi yang disajikan cukup komprehensif dan up-to-date. Sangat berguna bagi saya sebagai profesional IT.",
      author: "Rizky Nurfauzi",
    },
    {
      content:
        "Saya merekomendasikan situs ini kepada teman-teman saya yang ingin belajar database dari awal.",
      author: "Jessica Tan",
    },
    {
      content:
        "Setelah berkeliling mencari sumber belajar, akhirnya saya menemukan situs yang tepat. Sangat memuaskan!",
      author: "Farhan Abdillah",
    },
    {
      content:
        "Penjelasan konsep-konsep database yang disajikan sangat rinci dan mudah diikuti. Situs yang luar biasa!",
      author: "Lina Mulyani",
    },
    {
      content:
        "Saya berhasil mengerjakan tugas database dengan baik berkat bantuan situs ini. Terima kasih banyak!",
      author: "Andi Permana",
    },
  ];
 
</script>

<section class="py-10">
  <main class="container">
    <h1 class="text-center text-4xl font-semibold">Apa Kata Mereka ?</h1>
  </main>
  <div class="w-full overflow-hidden py-10 flex">
    <div class="flex w-fit px-4">
      {#each ulasan as item}
        <ReviewCard author={item.author} content={item.content} />
      {/each}
    </div>
    <div class="flex w-fit shrink-0 px-4">
      {#each ulasan as item}
        <ReviewCard author={item.author} content={item.content} />
      {/each}
    </div>
  </div>
  <div class="w-full overflow-hidden py-10 flex flex-row-reverse">
    <div class="flex w-fit px-4">
      {#each ulasan as item}
        <ReviewCard author={item.author} content={item.content} />
      {/each}
    </div>
    <div class="flex w-fit shrink-0 px-4 flex-row-reverse">
      {#each ulasan as item}
        <ReviewCard author={item.author} content={item.content} />
      {/each}
    </div>
  </div>
</section>
