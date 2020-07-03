<template>
  <div>
    <div>Todo</div>
    <div v-for="item in items" :key="item.name">
      <div class="item">
        <div>
          <span class="mgr">Task {{ item.name }}</span> Date {{ item.price }}
        </div>
      </div>
    </div>
    <div>
      <label>
        Todo
        <input type="text" v-model="newItemName" />
      </label>
      <label>
        Date
        <input type="date" v-model="newItemPrice" />
      </label>
      <button @click="addItem">Submit</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ItemList",
  data() {
    return {
      items: [],
      newItemName: "",
      newItemPrice: 0
    };
  },
  methods: {
    addItem() {
      this.items.push({ name: this.newItemName, price: this.newItemPrice });
    }
  }
};
</script>

<style>
.mgr {
  margin-right: 50px;
}
</style>
