<script>
  import Nav from "./components/Nav.svelte";
  import Hero from "./components/Hero.svelte";
  import Projects from "./components/Projects.svelte";
  import About from "./components/About.svelte";
  import Contact from "./components/Contact.svelte";
  import login from "./routes/Login.svelte";

  let routes = {
    "/login": login,
  };
  
  import { onMount } from "svelte";

  let form = { name: "", email: "", subject: "", message: "" };

  function submitForm() {
    alert(`Message sent by ${form.name}`);
  }

  let animate = false;

  onMount(() => {
    animate = true;
  });
</script>

<main class="bg-black text-white min-h-screen px-6 md:px-20 py-10 font-sans">
  <Nav {animate} />

  <Hero {animate} />

  <Projects />

  <About />
  <Contact {form} {submitForm} />


<!-- Router removed: Home route temporarily disabled to avoid import resolution error -->

</main>
