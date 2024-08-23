<script>
  import "../app.css";
  import Navbar from "../components/Navbar.svelte";
</script>

<main class="flex flex-col w-full">
  <div class="container w-[100vw] h-[20%]">
    <Navbar />
  </div>
  <div class="bg-[#1B264C]">
    <slot />
  </div>
</main>
