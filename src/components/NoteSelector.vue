<script>
export default {
  props: ["note"],
  data: function () {
    return {
      currentNote: {},
    };
  },
};
</script>

<template>
  <div class="note-selector">
    <p class="note-selector-title">{{ note.body }}</p>
    <p class="note-selector-timestamp">{{ note.timestamp }}</p>
  </div>
</template>
