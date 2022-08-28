<script>
import NoteSelector from "./NoteSelector.vue";

export default {
  components: { NoteSelector },
  data: function () {
    return {
      notes: [
        { id: 1, body: "This is a first test", timestamp: Date.now() },
        { id: 2, body: "This is a second test", timestamp: Date.now() },
        { id: 3, body: "This is a third test", timestamp: Date.now() },
        { id: 4, body: "This is a fourth test", timestamp: Date.now() },
      ],
    };
  },
};
</script>

<template>
  <div class="note-selectors">
    <!-- <div class="note-selector active">
      <p class="note-selector-title">First note...</p>
      <p class="note-selector-timestamp">Timestamp here...</p>
    </div> -->
    <!-- <div class="note-selector">
      <p class="note-selector-title">Second note...</p>
      <p class="note-selector-timestamp">Timestamp here...</p>
    </div>
    <div class="note-selector">
      <p class="note-selector-title">Third note...</p>
      <p class="note-selector-timestamp">Timestamp here...</p>
    </div> -->
    <!-- <div v-for="selector in selectors" v-bind:key="selector">
      {{ selector }}
    </div> -->
    <NoteSelector v-for="note in notes" v-bind:note="note" v-bind:key="note.id" />
  </div>
</template>
