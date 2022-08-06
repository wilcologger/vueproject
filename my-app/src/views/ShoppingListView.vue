<template>
  <div class="shopping-list">
    <div class="header">
      <h1>{{ heading }}</h1>
      <button
        v-if="hideEditing"
        @click="doEdit(false)"
        class="btn btn-secondary"
      >
        Cancel
      </button>
      <button v-else @click="doEdit(true)" class="btn btn-primary">
        Add item
      </button>
    </div>

    <form v-if="hideEditing" @submit.prevent="addShoppingItem">
      <div class="input-group mb-3">
        <input
          type="text"
          v-model="newShoppingItem"
          placeholder="Add shopping item"
          class="form-control"
        />
        <button
          v-bind:disabled="newShoppingItem.length === 0"
          class="btn btn-primary"
        >
          Save item
        </button>
      </div>
    </form>
    <ul>
      <li v-for="shoppingItem in filteredShoppingItems" :key="shoppingItem.id">
        <input type="checkbox" v-model="shoppingItem.done" />
        <span :class="{ done: shoppingItem.done }">
          {{ shoppingItem.text }}
        </span>
        <a @click="removeShoppingItem(shoppingItem)" class="btn btn-link">X</a>
      </li>
    </ul>

    <p v-if="shoppingItems.length === 0">
      Nice job! You've bought all your items!
    </p>
    <button
      v-else
      @click="hideCompleted = !hideCompleted"
      class="btn btn-secondary"
    >
      {{ hideCompleted ? "Show all" : "Hide completed" }}
    </button>
  </div>
</template>

<script>
let id = 0;

export default {
  data() {
    return {
      heading: "Shopping List",
      hideEditing: false,
      hideCompleted: false,
      newShoppingItem: "",
      shoppingItems: [
        // { id: id++, text: "Learn HTML" },
        // { id: id++, text: "Learn JavaScript" },
        // { id: id++, text: "Learn Vue" },
      ],
    };
  },
  computed: {
    filteredShoppingItems() {
      return this.hideCompleted
        ? this.shoppingItems.filter((s) => !s.done)
        : this.shoppingItems;
    },
  },
  methods: {
    doEdit(hideEditing) {
      this.hideEditing = hideEditing;
      this.newShoppingItem = "";
    },
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
