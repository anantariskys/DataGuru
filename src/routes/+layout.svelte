<script>
    import "../app.css";
  import Navbar from "../components/Navbar.svelte";
  </script>

<div>
    <Navbar/>
    <main class="container">
        <slot />
    </main>

</div>
