<script>
  export let showModal = false;
  export let closeModal;
</script>

{#if showModal}
  <div
    class="fixed inset-0 bg-gray-600 bg-opacity-50 overflow-y-auto h-full w-full"
    id="my-modal"
  >
    <div
      class="relative top-20 mx-auto p-5 border w-96 shadow-lg rounded-md bg-white"
    >
      <div class="mt-3 text-left">
        <div class="flex justify-between items-center pb-3">
          <p class="text-2xl font-bold">Connection Settings</p>
          <div class="modal-close cursor-pointer z-50" on:click={closeModal}>
            <svg
              class="fill-current text-black"
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="18"
              viewBox="0 0 18 18"
            >
              <path
                d="M14.53 3.53a.75.75 0 0 0-1.06-1.06L9 6.94 4.53 2.47a.75.75 0 1 0-1.06 1.06L7.94 9l-4.47 4.47a.75.75 0 0 0 1.06 1.06L9 11.06l4.47 4.47a.75.75 0 0 0 1.06-1.06L10.06 9l4.47-4.47z"
              ></path>
            </svg>
          </div>
        </div>
        <form>
          <div class="mb-2">
            <label for="host" class="block text-sm font-medium text-gray-700"
              >Host</label
            >
            <input
              type="text"
              id="host"
              name="host"
              class="mt-1 block w-full border-gray-300 rounded-md shadow-sm sm:text-sm"
            />
          </div>
          <div class="mb-2">
            <label for="port" class="block text-sm font-medium text-gray-700"
              >Port</label
            >
            <input
              type="text"
              id="port"
              name="port"
              class="mt-1 block w-full border-gray-300 rounded-md shadow-sm sm:text-sm"
            />
          </div>
          <div class="mb-2">
            <label
              for="username"
              class="block text-sm font-medium text-gray-700">Username</label
            >
            <input
              type="text"
              id="username"
              name="username"
              class="mt-1 block w-full border-gray-300 rounded-md shadow-sm sm:text-sm"
            />
          </div>
          <div class="mb-2">
            <label
              for="password"
              class="block text-sm font-medium text-gray-700">Password</label
            >
            <input
              type="password"
              id="password"
              name="password"
              class="mt-1 block w-full border-gray-300 rounded-md shadow-sm sm:text-sm"
            />
          </div>
          <hr class="my-4" />
          <div class="mb-2">
            <label
              for="connection-url"
              class="block text-sm font-medium text-gray-700"
              >Connection URL</label
            >
            <input
              type="text"
              id="connection-url"
              name="connection-url"
              class="mt-1 block w-full border-gray-300 rounded-md shadow-sm sm:text-sm"
            />
          </div>
          <div class="flex justify-end gap-2 mt-4">
            <button
              type="button"
              class="bg-gray-500 hover:bg-gray-700 text-white py-2 px-4 rounded-full"
              on:click={closeModal}>Cancel</button
            >
            <button
              type="button"
              class="bg-gray-500 hover:bg-gray-700 text-white py-2 px-4 rounded-full"
              >Test</button
            >
            <button
              type="button"
              class="bg-gray-500 hover:bg-gray-700 text-white py-2 px-4 rounded-full"
              >Save</button
            >
          </div>
        </form>
      </div>
    </div>
  </div>
{/if}

<style>
  .modal-close svg:hover {
    cursor: pointer;
  }
</style>
