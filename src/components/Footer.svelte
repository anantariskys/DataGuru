<script>
  import Icon from "@iconify/svelte";
import Logo from "../assets/Logo.png";
</script>

<footer class="bg-[#F6F5FF]">
  <main class="py-20 container space-y-4">
    <img src={Logo} draggable="false" alt="Logo" />
    <div class="flex justify-between">
      <div class="space-y-8">
        <div class="space-y-2 max-w-72">
          <h3 class="font-bold text-xl">Malang</h3>
          <p>Fakultas Ilmu Komputer Universitas Brawijaya, Malang, Indonesia</p>
        </div>
        <div class="space-y-2 max-w-72">
          <h3 class="font-bold text-xl">Bima</h3>
          <p>JK House, Kota Bima 3004, Indonesia</p>
        </div>
      </div>
      <div class="flex justify-end gap-24">
        <div class="space-y-2 max-w-72">
          <h3 class="font-bold text-xl">Products</h3>
          <p>Materi</p>
          <p>Quiz</p>
          <p>Blog</p>
        </div>
        <div class="space-y-2 max-w-72">
          <h3 class="font-bold text-xl">Company</h3>
          <p>Contact Us</p>
        </div>
        <div class="space-y-2 max-w-72">
          <h3 class="font-bold text-xl">Other</h3>
          <p>Privacy & Policy</p>
          <p>Terms & Condition</p>
        </div>
        <div class="space-y-2 max-w-72">
          <h3 class="font-bold text-xl">Social Media</h3>
          <p>Instagram</p>
          <p>Youtube Channel</p>
          <p>Telegram</p>
          <p>Facebook Page</p>
        </div>
      </div>
    </div>
    <div class="space-y-2">
        <p class="text-center text-lg">Ikuti kami di</p>
        <div class="flex w-fit mx-auto gap-4">
            <Icon icon='mdi:instagram' class='text-3xl'/>
            <Icon icon='mdi:youtube' class='text-3xl'/>
            <Icon icon='ic:baseline-telegram' class='text-3xl'/>
            <Icon icon='ic:baseline-facebook' class='text-3xl'/>
        </div>
    </div>
    <p class="text-sm text-center">© 2024 DataGuru · Made with ❤️ by Tim JKtole</p>
  </main>
</footer>
