<script>
  import NewNotebookHeader from '../../components/NewNotebookHeader.svelte';
  // import { onMount } from 'svelte';
  // import * as monaco from 'vite-plugin-monaco-editor';

  // /**
  //  * @type {{ dispose: () => void; getValue: () => any; }}
  //  */
  // let editor;
  // /**
  //  * @type {null}
  //  */
  // let results = null;

  // onMount(() => {
  //   // @ts-ignore
  //   editor = monaco.editor.create(document.getElementById('editor-container'), {
  //     value: '',
  //     language: 'plaintext',
  //     theme: 'vs-dark',
  //     automaticLayout: true,
  //   });

  //   return () => {
  //     editor.dispose();
  //   };
  // });

  // @ts-ignore
  // async function executeCommands() {
  //   const commands = editor.getValue();
  //   const response = await fetch('/api/execute', {
  //     method: 'POST',
  //     headers: { 'Content-Type': 'application/json' },
  //     body: JSON.stringify({ commands }),
  //   });
  //   results = await response.json();
  // }

  const titles = [
    'My Past Skin Notebook',
    'My Fitting Mine Notebook',
    'My Amazing Journey Notebook',
    'My Adventurous Tale Notebook',
    'My Creative Ideas Notebook',
    'My Flimsy Weird Notebook',
    'My Waterlogged Current Notebook',
    'My Quarterly Advice Notebook',
  ];

  function getRandomTitle() {
    return titles[Math.floor(Math.random() * titles.length)];
  }

  // @ts-ignore
  let title = getRandomTitle();
</script>

<NewNotebookHeader />

<div class="flex items-center my-2">
  <span
    class="invisible absolute text-3xl overflow-hidden"
    style="height: 0px;"
  >
    {titles}
  </span>
</div>

<div>
  <div class="shadow-lg">
    <div class="relative pb-2">
      <div style="height: 150px;">
        <div class="relative">
          <div class="absolute top-2 right-2 flex">
            <div class="flex flex-row">
              <div>
                <button
                  type="button"
                  class="text-xs flex items-center justify-center p-1 transition ease-in duration-200 rounded-full hover:bg-gray-800 hover:text-white border-2 border-gray-900 focus:outline-none mx-0.5 opacity-20 hover:opacity-100"
                >
                  <span
                    class="text-center -mr-px material-icons"
                    style="font-size: 17px;">list</span
                  >
                </button>
              </div>
              <div>
                <button
                  type="button"
                  class="text-xs flex items-center justify-center p-1 transion ease-in duration-200 rounded-full hover:bg-gray-800 hover:text-white border-2 border-gray-900 focus:outline-none mx-0.5 opacity-20 hover:opacity-100"
                >
                  <span
                    class="text-center -mr-px material-icons"
                    style="font-size: 17px;">format_paint</span
                  >
                </button>
              </div>
            </div>
            <div class="flex flex-row">
              <button
                type="button"
                class="text-xs flex items-center justify-center p-1 transion ease-in duration-200 rounded-full hover:bg-gray-800 hover:text-white border-2 border-gray-900 focus:outline-none mx-0.5 opacity-20 hover:opacity-100"
              >
                <span
                  class="text-center -mr-px material-icons"
                  style="font-size: 17px;">arrow_upward</span
                >
              </button>
              <button
                type="button"
                class="text-xs flex items-center justify-center p-1 transion ease-in duration-200 rounded-full hover:bg-gray-800 hover:text-white border-2 border-gray-900 focus:outline-none mx-0.5 opacity-20 hover:opacity-100"
              >
                <span
                  class="text-center -mr-px material-icons"
                  style="font-size: 17px;">arrow_downward</span
                >
              </button>
              <button
                type="button"
                class="text-xs flex items-center justify-center p-1 transion ease-in duration-200 rounded-full hover:bg-gray-800 hover:text-white border-2 border-gray-900 focus:outline-none mx-0.5 opacity-20 hover:opacity-100"
              >
                <span
                  class="text-center -mr-px material-icons"
                  style="font-size: 17px;">close</span
                >
              </button>
            </div>
          </div>
        </div>
        <div
          class="wrapper svelte-v1brr"
          style="--left-panel-size: 50%; --right-panel-size: 50%; --min-left-panel-size: 0; --min-right-panel-size: 0;"
        >
          <div class="left svelte-v1brrr"></div>
          <div
            class="separator h-full w-2 select-none cursor-col-resize z-20 bg-gray-400 svelte-v1brrr"
          ></div>
          <div class="right svelte-v1brrr"></div>
        </div>
      </div>
      <div
        class="absolute bottom-0 w-full select-none cursor-row resize h-2 z-20 bg-gray-400"
      ></div>
    </div>
  </div>
</div>

<style>
  .material-icons {
    font-size: 24px;
  }
</style>
