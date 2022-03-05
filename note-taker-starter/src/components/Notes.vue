<template>
  <div class="note text-start">
    <!-- Add a new Note Button -->
    <button class="mt-4 mx-3 rounded-pill">
      <i class="fas fa-plus fs-4"></i>
    </button>

    <!-- Main note area -->
    <div class="note-header">
      <div class="noteList">
        <h3>My Notes</h3>
        <ul>
          <li
            class="d-flex align-items-center py-2 border-bottom fw-bold justify-content-between"
          >
            <span class="btn text-white">Title</span>
            <button class="btn bg-danger rounded-pill p-0 px-3">X</button>
          </li>
        </ul>
      </div>
      <div class="note-display">
        <h4>Title</h4>
        <p>Description</p>
        <button class="me-3">Edit</button>
        <button>Close Note</button>
      </div>
    </div>

    <!-- Note creation/edit form -->
    <div class="noteForm text-center">
      <label class="form-label">Title:</label><br />
      <input type="text" class="form-control" minlength="2" />
      <label class="form-label">Description:</label>
      <textarea ref="noteDesc" class="form-control"></textarea>
      <button class="mt-3 me-3">Save</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyNotes",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.note-header {
  display: flex;
  justify-content: space-around;
}
.noteForm {
  border-right: 1px solid #000;
  padding: 0 2rem 2rem 2 rem;
  /* opacity: 0; */
  transition: 200ms ease;
}
.noteForm.display {
  opacity: 1;
}
.note-display {
  /* opacity: 0; */
  transition: 200ms ease;
  text-align: start;
  padding: 2rem;
  max-width: 320px;
  width: 320px;
  word-wrap: break-word;
}
.note-display.display {
  opacity: 1;
}
.noteForm * {
  margin: 0 auto;
}
.noteList ul {
  list-style: none;
  padding: 0;
}
.noteList {
  padding: 2rem;
  width: 50%;
  text-align: start;
}

input[type="text"],
textarea {
  width: 300px;
}
button {
  padding: 0.5rem 1rem;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-weight: 600;
  border: none;
  background: #2c3e7f;
  border-radius: 10px;
  transition: 300ms ease;
  color: #ddd;
}
button:hover {
  background: #2c3eff;
  color: #fff;
  transform: translateY(2px);
}
</style>
