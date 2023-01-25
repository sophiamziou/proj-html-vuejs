<script>
export default {};
</script>
<template>
  <div class="container-fluid search_bar">
    <div class="row h-100">
      <div class="col">
        <div
          class="h-100 d-flex align-items-center justify-content-between p-4"
        >
          <input
            type="search"
            class="form-control"
            placeholder="Search..."
            aria-label="Search"
          />
          <i class="fa-solid fa-xmark fs-5 mx-2"></i>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.search_bar {
  height: 100px;
  background: white;
  input {
    border: none;
  }
  i:hover {
    cursor: pointer;
    color: #ff4612;
  }
}
</style>
