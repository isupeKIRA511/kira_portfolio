<script>
  import { onMount } from "svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";

  gsap.registerPlugin(ScrollTrigger);

  let projectsSection;

  onMount(() => {
    const projectItems = projectsSection.querySelectorAll(".project-item");

    projectItems.forEach((item) => {
      const image = item.querySelector("img");
      const content = item.querySelector(".project-content");

      gsap.from(image, {
        x: -100,
        opacity: 0,
        duration: 1,
        scrollTrigger: {
          trigger: item,
          start: "top 85%",
        },
      });

      gsap.from(content, {
        x: 100,
        opacity: 0,
        duration: 1,
        delay: 0.2,
        scrollTrigger: {
          trigger: item,
          start: "top 85%",
        },
      });
    });
  });
</script>

<section id="work" class="mb-16" bind:this={projectsSection}>
  <h3 class="text-white text-3xl font-bold mb-4">FEATURED PROJECTS</h3>
  <p class="text-gray-400 mb-8 max-w-xl">
    Here are some of the selected projects that showcase my passion for front-end development.
  </p>

  <div class="project-item bg-gray-900 p-6 rounded-lg mb-10 flex flex-col md:flex-row gap-8">
    <img src="/2025-11-21 23.32.23.jpg" alt="Calculator Project" class="md:w-1/2 rounded-lg" />
    <div class="project-content md:w-1/2 flex flex-col justify-between">
      <div>
        <span class="inline-block bg-gray-700 text-xs rounded-full px-3 py-1 mb-2">Conceptual Work</span>
        <h4 class="text-xl font-semibold mb-2">Scientific Calculator</h4>
        <p class="text-gray-400 mb-4">
          It takes basic arithmetic operations and extends them to include scientific functions such as trigonometry, logarithms, and exponentiation.
        </p>
        <div class="text-gray-500 text-sm mb-4">
          <div>Front-end Developer</div>
        </div>
      </div>
      <div class="flex space-x-6 text-lime-400 text-sm font-semibold">
        <a href="https://github.com/isupeKIRA511" target="_blank" class="hover:underline flex items-center gap-1">
          SEE ON GITHUB ↗
        </a>
      </div>
    </div>
  </div>

  <div class="project-item bg-gray-900 p-6 rounded-lg mb-10 flex flex-col md:flex-row gap-8">
    <img src="/2025-11-21 23.41.17.jpg" alt="Shopping Cart" class="md:w-1/2 rounded-lg" />
    <div class="project-content md:w-1/2 flex flex-col justify-between">
      <div>
        <h4 class="text-xl font-semibold mb-2">Shopping Cart</h4>
        <p class="text-gray-400 mb-4">
          Shopping cart application that allows users to add, remove, and update items in their cart.
        </p>
        <div class="text-gray-500 text-sm mb-4">
          <div>Front-end Developer</div>
        </div>
      </div>
      <div class="flex space-x-6 text-lime-400 text-sm font-semibold">
        <a href="https://github.com/isupeKIRA511" target="_blank" class="hover:underline flex items-center gap-1">
          SEE ON GITHUB ↗
        </a>
      </div>
    </div>
  </div>

  <div class="project-item bg-gray-900 p-6 rounded-lg mb-10 flex flex-col md:flex-row gap-8">
    <img src="/2025-11-21 23.46.52.jpg" alt="Portfolio" class="md:w-1/2 rounded-lg" />
    <div class="project-content md:w-1/2 flex flex-col justify-between">
      <div>
        <span class="inline-block bg-gray-700 text-xs rounded-full px-3 py-1 mb-2">Challenge</span>
        <h4 class="text-xl font-semibold mb-2">Portfolio</h4>
        <p class="text-gray-400 mb-4">
          Personal portfolio website to showcase my projects, skills, and experience as a front-end developer.
        </p>
        <div class="text-gray-500 text-sm mb-4">
          <div>Front-end Developer</div>
        </div>
      </div>
      <div class="flex space-x-6 text-lime-400 text-sm font-semibold">
        <a href="https://github.com/isupeKIRA511" target="_blank" class="hover:underline flex items-center gap-1">
          SEE ON GITHUB ↗
        </a>
      </div>
    </div>
  </div>
</section>
