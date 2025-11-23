<script>
    import { Linkedin, Github, Twitter, Instagram } from "lucide-svelte";

    export let form;
    export let submitForm;
</script>

<section
    id="contact"
    class="mb-10 flex flex-col md:flex-row md:justify-between gap-10"
>
    <div class="flex flex-col space-y-4 max-w-md">
        <h3 class="text-white text-3xl font-bold">LET’S CONNECT</h3>

        <p>
            Say hello at <a
                href="mailto:isupekira511@gmail.com"
                class="cursor-pointer underline text-lime-400"
                >isupekira511@gmail.com</a
            >
            <br />
            For more info, here’s my
            <a href="#intro" class="cursor-pointer underline text-lime-400">resume</a>
        </p>

        <div class="flex space-x-4 text-lime-400">
            <a class="hover:text-lime-600"><Linkedin class="w-6 h-6" /></a>
            <a class="hover:text-lime-600"><Github class="w-6 h-6" /></a>
            <a class="hover:text-lime-600"><Twitter class="w-6 h-6" /></a>
            <a class="hover:text-lime-600"><Instagram class="w-6 h-6" /></a>
        </div>
    </div>

    <form
        on:submit|preventDefault={submitForm}
        class="flex flex-col space-y-4 max-w-lg w-full"
    >
        <input
            type="text"
            placeholder="Name"
            bind:value={form.name}
            class="p-3 rounded bg-gray-800 border border-gray-700"
            required
        />
        <input
            type="email"
            placeholder="Email"
            bind:value={form.email}
            class="p-3 rounded bg-gray-800 border border-gray-700"
            required
        />
        <input
            type="text"
            placeholder="Subject"
            bind:value={form.subject}
            class="p-3 rounded bg-gray-800 border border-gray-700"
            required
        />
        <textarea
            rows="5"
            placeholder="Message"
            bind:value={form.message}
            class="p-3 rounded bg-gray-800 border border-gray-700"
            required
        ></textarea>

        <button
            type="submit"
            class="self-start bg-lime-400 text-black font-semibold px-8 py-2 rounded-full hover:bg-lime-600 transition"
        >
            SUBMIT
        </button>
    </form>
</section>
