<template>
  <div class="note">
    <!-- Add a new Note Button -->
    <button class="my-4 mx-lg-3 rounded-pill">
      <i class="fas fa-plus fs-3"></i>
    </button>
    <!-- Main note area -->
    <div class="note-header ps-2 my-4">
      <div class="noteList me-lg-5 p-lg-3 mb-2">
        <h3 class="text-center">My Notes</h3>
        <ul class="note-item-list mx-auto">
          <li
            class="note-item d-flex align-items-center py-2 border-bottom fw-bold justify-content-between"
          >
            <span class="btn text-white text-start">Title</span>
            <button class="btn bg-danger">X</button>
          </li>
        </ul>
      </div>
      <div class="note-display text-center">
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
      <textarea class="form-control"></textarea>
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
  justify-content: center;
  flex-wrap: wrap;
  align-items: center;
}
.noteForm {
  padding: 0 2rem 2rem 2 rem;
  /* opacity: 0; */
  transition: 200ms ease;
  max-width: 400px;
  margin: 0 auto;
}
.noteForm.display {
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
  min-width: 300px;
  text-align: start;
}
.note-item-list {
  max-width: 350px;
}
.note-display {
  /* opacity: 0; */
  transition: 200ms ease;
  text-align: start;
  max-width: 450px;
  width: 450px;
  word-wrap: break-word;
}
.note-display.display {
  opacity: 1;
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
