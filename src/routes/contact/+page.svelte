<script>
  let name = '';
  let company = '';
  let age = '';
  let message = '';
  function submitForm() {
    // handle submission (e.g., send to email API)
    console.log({ name, company, age, message });
  }
</script>

<h1 class="text-3xl font-bold mb-6">Contact Me</h1>
<form on:submit|preventDefault={submitForm} class="max-w-lg mx-auto space-y-4">
  <div>
    <label class="block text-gray-700 mb-1">Name / Company / Age</label>
    <input type="text" bind:value={name} placeholder="Name" class="w-full border rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500" />
  </div>
  <div>
    <label class="block text-gray-700 mb-1">Message</label>
    <textarea bind:value={message} rows="6" placeholder="Your message..." class="w-full border rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
  </div>
  <button type="submit" class="w-full bg-blue-600 text-white py-3 rounded-xl hover:bg-blue-700 transition font-medium">
    Send Message
  </button>
</form>