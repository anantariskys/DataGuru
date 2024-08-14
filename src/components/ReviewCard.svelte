<script>
    import Quotes from "../assets/Quotes.png";
    export let content;
    export let author;
  </script>
  
  <div
    class="w-96 flex-shrink-0 px-10 py-4 space-y-3 rounded-2xl shadow-md text-white bg-gradient-to-b from-[#7052FF] to-[#A368FE] mx-4"
  >
    <img src={Quotes} draggable="false" alt="quotes" />
    <p class="">{content}</p>
    <p class="font-bold">~ {author}</p>
  </div>