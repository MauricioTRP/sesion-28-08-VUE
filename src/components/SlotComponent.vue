<template>
  <button>
    <slot />
  </button>
</template>
<style scoped>
button {
  background-color: darkgreen;
  box-shadow: 4px 4px 20px 4px black;
  color: white;
  padding: 1.5rem 2rem;
  text-shadow: 1px 1px 1px black;
  border-radius: 15px;
}
</style>
