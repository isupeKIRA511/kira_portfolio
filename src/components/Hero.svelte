<script>
  import { Linkedin, Github, Instagram } from "lucide-svelte";
  export let animate = false;
  import { gsap } from "gsap";

  $: if (animate) {
    gsap.from("#intro", {
      x: -200,
      opacity: 0,
      duration: 1.5,
      ease: "power3.out"
    });
  }
</script>

<section id="intro" class="flex flex-col md:flex-row md:items-center gap-10 mb-16 mt-20">
  <div class="flex-1 space-y-4 max-w-lg">
    <h2 class="text-4xl font-extrabold leading-tight">
      HI, I AM <br />
      <span class="text-lime-400 ">BARIQ AQEEL</span>
    </h2>

    <p class="text-gray-400">
      A based front-end developer passionate about building <br />
      accessible and user friendly websites.
    </p>

    <button class="bg-lime-400 text-black font-semibold px-6 py-2 rounded-full hover:bg-lime-600 transition">
      CONTACT ME
    </button>

    <div class="flex space-x-4 mt-4">
      <a href="#" class="bg-gray-800 p-3 rounded-full hover:bg-lime-600 transition">
        <Linkedin class="w-6 h-6" />
      </a>
      <a href="https://github.com/isupeKIRA511" target="_blank" class="bg-gray-800 p-3 rounded-full hover:bg-lime-600 transition">
        <Github class="w-6 h-6" />
      </a>
      <a href="https://instagram.com/isupekira"
  target="_blank" class="bg-gray-800 p-3 rounded-full hover:bg-lime-600 transition">
        <Instagram class="w-6 h-6" />
      </a>
    </div>
  </div>

  <div class="flex justify-center md:justify-end flex-1 mr-20">
    <div class="flex justify-end max-w-sm rounded-lg overflow-hidden bg-gray-300 translate-y-5 shadow-lg">
      <img src="2025-11-21 22.39.56.jpg" alt="Bariq Aqeel" class="w-full h-full object-cover" />
    </div>
  </div>
</section>
