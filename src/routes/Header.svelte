<script>
  import { goto } from "$app/navigation";
</script>

<div class="sticky top-0 z-30">
  <nav class="bg-white dark:bg-gray-800 shadow">
    <div class="max-w-7xl mx-auto px-16">
      <div class="flex items-center justify-between h-11">
        <a href="/">
          <h1 class="text-xl">redis-book</h1>
        </a>
        <div class="flex">
          <div class="flex gap-4">
            <button
              type="button"
              class="bg-gray-500 hover:bg-gray-700 disabled:bg-gray-300 py-2 px-4 flex justify-center items-center text-white transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none rounded-full flex items-center align-center h-8"
              on:click={() => goto("/upload-notebook")}
            >
              <span
                class="text-center mr-1 material-icons"
                style="font-size:20px;">add</span
              >Upload Notebook
            </button>
            <button
              type="button"
              class="bg-blue-500 hover:bg-blue-700 disabled:bg-blue-300 py-2 px-4 flex justify-center items-center text-white transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none rounded-full flex items-center align-center h-8"
              on:click={() => goto("/new-notebook")}
            >
              <span
                class="text-center mr-1 material-icons"
                style="font-size: 20px;">add</span
              >
              New Notebook
            </button>
          </div>
        </div>
      </div>
    </div>
  </nav>
</div>

<style>
  .material-icons {
    font-size: 24px;
  }
</style>
