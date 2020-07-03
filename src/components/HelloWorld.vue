<template>
  <div>
    <h1>{{ msg }}</h1>
    <counter />
    <item-list />
    <br />
    <todo />
  </div>
</template>

<script>
import Counter from "./Counter.vue";
import ItemList from "./ItemList.vue";
import todo from "./todo.vue";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components: {
    Counter,
    ItemList,
    todo
  }
};
</script>
