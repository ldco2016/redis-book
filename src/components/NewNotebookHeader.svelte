<script>
  import { goto } from '$app/navigation';
  import ConnectModal from './ConnectModal.svelte';

  let showModal = false;

  function openModal() {
    showModal = true;
  }

  function closeModal() {
    showModal = false;
  }
</script>

<div class="sticky top-0 z-30">
  <nav class="bg-white dark:bg-gray-800 shadow">
    <div class="max-w-7xl mx-auto px-16">
      <div class="flex items-center justify-between h-11">
        <button
          type="button"
          class="flex items-center text-blue-500"
          on:click={() => goto('/')}
        >
          <span class="material-icons" style="font-size:20px;"
            >chevron_left</span
          >
          Back
        </button>
        <div class="flex gap-4">
          <button
            type="button"
            class="bg-gray-500 hover:bg-gray-700 disabled:bg-gray-300 py-2 px-4 flex justify-center items-center text-white transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none rounded-full flex items-center align-center h-8"
            on:click={openModal}
          >
            <span
              class="text-center mr-1 material-icons"
              style="font-size:20px;">settings</span
            >
            Conectar
          </button>
          <button
            type="button"
            class="bg-blue-500 hover:bg-blue-700 disabled:bg-blue-300 py-2 px-4 flex justify-center items-center text-white transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none rounded-full flex items-center align-center h-8"
          >
            <span
              class="text-center mr-1 material-icons"
              style="font-size:20px;">play_arrow</span
            >
            Ejecutar Todo
          </button>
        </div>
      </div>
    </div>
  </nav>
</div>

<ConnectModal {showModal} {closeModal} />

<style>
  .material-icons {
    font-size: 24px;
  }
</style>
