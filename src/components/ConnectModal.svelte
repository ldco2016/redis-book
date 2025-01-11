<script>
  export let showModal = false;
  export let closeModal;
</script>

{#if showModal}
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <!-- svelte-ignore a11y-no-static-element-interactions -->
  <div
    class="fixed inset-0 bg-gray-600 bg-opacity-50 overflow-y-auto flex justify-center items-center"
    id="my-modal"
    on:click={closeModal}
  >
    <div class="relative w-96 p-5 shadow-lg rounded-md bg-white">
      <div class="bg-gray-50 rounded-lg p-4 bg-white shadow">
        <div class="w-full mx-auto pt-4 pb-4 px-4 z-20">
          <div class="flex flex-col gap-4">
            <div class="flex flex-col gap-4">
              <h1 class="text-3xl">Connection Settings</h1>
              <div class="flex gap-4">
                <div class="w-1/2">
                  <label for="name-with-label">Host</label>
                  <input
                    type="text"
                    class="rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent"
                    autocomplete="off"
                    autocorrect="off"
                    autocapitalize="off"
                    spellcheck="false"
                  />
                </div>
                <div class="w-1/2">
                  <label for="name-with-label">Port</label>
                  <input
                    type="text"
                    class="rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent"
                    autocomplete="off"
                    autocorrect="off"
                    autocapitalize="off"
                    spellcheck="false"
                  />
                </div>
              </div>
              <div class="flex gap-4">
                <div class="w-1/2">
                  <label for="name-with-label">Usuario</label>
                  <input
                    type="text"
                    class="rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent"
                    autocomplete="off"
                    autocorrect="off"
                    autocapitalize="off"
                    spellcheck="false"
                  />
                </div>
                <div class="w-1/2">
                  <label for="password">Contraseña</label>
                  <input
                    type="password"
                    class="rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-purple-600 focus:border-transparent"
                    autocomplete="off"
                    autocorrect="off"
                    autocapitalize="off"
                    spellcheck="false"
                  />
                </div>
              </div>
            </div>
            <div
              class="relative w-full mt-5 mb-3 flex justify-center items-center"
            >
              <div
                class="w-1/2 mx-5 right-0 left-0 border-gray-400 border-b"
              ></div>
              <div class="z-10">Or...</div>
              <div
                class="w-1/2 mx-5 right-0 left-0 border-gray-400 border-b"
              ></div>
            </div>
            <div class="flex flex-col gap-4">
              <div class="w-full">
                <label for="name-with-label">Connection URL</label>
                <input
                  type="text"
                  class="rounded-lg flex-1 appearance-none border border-gray-300 w-full py-2 px-4 bg-white text-gray-700 placeholder-gray-400 shadow-sm text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent"
                  autocomplete="off"
                  autocorrect="off"
                  autocapitalize="off"
                  spellcheck="false"
                />
              </div>
            </div>
            <div class="flex justify-end gap-3">
              <button
                type="button"
                class="bg-gray-500 hover:bg-gray-700 disabled:bg-gray-300 py-2 px-4 flex justify-center items-center text-white transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none rounded-full flex items-center align-center"
                on:click={closeModal}>Cancelar</button
              >
              <button
                type="button"
                class="bg-blue-500 hover:bg-blue-700 disabled:bg-blue-300 py-2 px-4 flex justify-center items-center text-white transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none rounded-full flex items-center align-center"
                >Probar</button
              >
              <button
                type="button"
                class="bg-green-500 hover:bg-green-700 disabled:bg-green-300 py-2 px-4 flex justify-center items-center text-white transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none rounded-full flex items-center align-center"
                >Guardar</button
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
{/if}

<style>
  .modal-close svg:hover {
    cursor: pointer;
  }
</style>
