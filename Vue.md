## Emit

```js
// Test.vue
<script setup lang="ts">
const emit = defineEmits(["btnClick"]);

const handleData = () => {
    emit("btnClick", "Sahos Vai ami asi");
}
</script>

<template>
  <div>
    <button @click="handleData">Show name</button>
  </div>
</template>
```

```js
// App.vue
<script setup>
import Test from "./components/Test.vue";

const getMessage = (data) => {
  console.log(data);
};
</script>

<template>
  <Test @btn-click="getMessage" />
</template>


// Output : Sahos vai ami asi
```
