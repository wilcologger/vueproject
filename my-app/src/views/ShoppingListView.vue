<template>
  <div class="shopping-list">
    <form @submit.prevent="addShoppingItem">
      <input
        type="text"
        v-model="newShoppingItem"
        placeholder="Add shopping item"
        class="form-control"
      />
      <button class="btn btn-primary">Add item</button>
    </form>
    <ul>
      <li v-for="shoppingItem in shoppingItems" :key="shoppingItem.id">
        {{ shoppingItem.text }}
        <a @click="removeShoppingItem(shoppingItem)" class="btn btn-link">X</a>
      </li>
    </ul>
  </div>
</template>

<script>
let id = 0;

export default {
  data() {
    return {
      newShoppingItem: "",
      shoppingItems: [
        { id: id++, text: "Learn HTML" },
        { id: id++, text: "Learn JavaScript" },
        { id: id++, text: "Learn Vue" },
      ],
    };
  },
  methods: {
    addShoppingItem() {
      this.shoppingItems.push({ id: id++, text: this.newShoppingItem });
      this.newShoppingItem = "";
    },
    removeShoppingItem(shoppingItem) {
      this.shoppingItems = this.shoppingItems.filter((s) => s !== shoppingItem);
    },
  },
};
</script>
