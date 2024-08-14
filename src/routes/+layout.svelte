<script>
    import "../app.css";
  import Footer from "../components/Footer.svelte";
  import Navbar from "../components/Navbar.svelte";
  </script>

<div>
    <Navbar/>
    <main class="">
        <slot />
    </main>
    <Footer/>


</div>
