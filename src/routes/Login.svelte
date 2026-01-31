<script>
  let form = { email: "", password: "" };

  function submitLogin() {
    alert(`Logged in as ${form.email}`);
  }
</script>

<main class="bg-black min-h-screen flex items-center justify-center px-6">
  <div class="bg-neutral-900 p-10 rounded-2xl shadow-lg w-full max-w-md">
    <h1 class="text-3xl font-bold text-green-500 mb-6 text-center">Login</h1>

    <form on:submit|preventDefault={submitLogin} class="flex flex-col gap-4">
      <input
        type="email"
        placeholder="Email"
        bind:value={form.email}
        class="p-3 rounded bg-black border border-green-500 text-white focus:outline-none focus:ring-2 focus:ring-green-500"
        required
      />
      <input
        type="password"
        placeholder="Password"
        bind:value={form.password}
        class="p-3 rounded bg-black border border-green-500 text-white focus:outline-none focus:ring-2 focus:ring-green-500"
        required
      />
      <button
        type="submit"
        class="bg-green-500 hover:bg-green-400 text-black font-semibold rounded-xl py-3 mt-2 transition-colors"
      >
        Log In
      </button>
    </form>
  </div>
</main>
