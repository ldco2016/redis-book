<script>
  const titles = [
    "My Past Skin Notebook",
    "My Fitting Mine Notebook",
    "My Amazing Journey Notebook",
    "My Adventurous Tale Notebook",
    "My Creative Ideas Notebook",
    "My Flimsy Weird Notebook",
    "My Waterlogged Current Notebook",
  ];

  function getRandomTitle() {
    return titles[Math.floor(Math.random() * titles.length)];
  }

  let title = getRandomTitle();
</script>

<div class="flex items-center my-2">
  <span class="invisible absolute text-3xl overflow-hidden" style="height: 0px;"
    >{title}</span
  >
</div>
