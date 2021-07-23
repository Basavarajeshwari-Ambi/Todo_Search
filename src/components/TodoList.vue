<template>
  <div class="List"></div>
</template>

<script>
export default {};
</script>


<style lang="scss" scoped>
ul,
li {
  margin: 0;
  padding: 0;
}

li {
  border-top: rgb(112, 106, 106) solid 1px;
  display: flex;
  justify-content: space-between;

  &:first-child {
    border-top: none;
  }

  label {
    padding: 8px 4px;
    width: 100%;
    display: cursor;

    &:hover {
      background: rgb(219, 217, 218);
    }
  }
}

.completed {
  label {
    text-decoration: line-through;
    color: #aaa;
    margin-right: 1em;
  }
}

.empty {
  font-size: 14px;
  color: rgb(71, 70, 70);
}
button.responses {
  background-color: transparent;
  color: white;
  border: none;
}

input[type="checkbox"] {
  display: none;
}
</style>
