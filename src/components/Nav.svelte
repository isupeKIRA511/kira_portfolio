<script>
  import { gsap } from "gsap";

  export let animate = false;

  $: if (animate) {
    gsap.from("header", {
      y: -100,
      opacity: 0,
      duration: 1,
      ease: "power3.out"
    });
  }
</script>

<header class="fixed top-0 left-0 w-full flex justify-between items-center z-50 bg-black/90 px-6 py-3 shadow-md">
  <h1 class="font-bold text-xl ml-10">BARIQ AQEEL</h1>

  <nav class="space-x-6 text-sm font-bold mr-20">
    <a href="#work" class="hover:text-lime-500">Projects</a>
    <a href="#about" class="hover:text-lime-500">About</a>
    <a href="#contact" class="hover:text-lime-500">Contact</a>
  </nav>
</header>
