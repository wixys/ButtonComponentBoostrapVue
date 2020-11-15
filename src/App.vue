<template>
  <div id="app">
    <Button
      :labelName="'Open link'"
      :variant="'outline-success'"
      :icon="'arrow-right-circle'"
      :iconClass="'ml-3'"
      :size="'lg'"
      :link="'https://v3.vuejs.org/guide/instance.html'"
      :pill="false"
      :squared="true"
    />
    <Button
      :labelName="'Say Hello'"
      :variant="'primary'"
      :icon="'code'"
      :iconClass="'ml-2'"
      :size="'sm'"
      :setFunction="sayHello"
      :pill="false"
      :squared="false"
    />
    <Button
      :labelName="'Say bye'"
      :variant="'danger'"
      :icon="'code'"
      :iconClass="'ml-2'"
      :size="'md'"
      :setFunction="sayBye"
      :pill="true"
      :squared="false"
    />
    <Button
      :labelName="'Do something'"
      :variant="'warning'"
      :icon="'alarm'"
      :iconClass="'ml-2'"
      :size="'lg'"
      :setFunction="doSomething"
      :pill="false"
      :squared="true"
    />
    <Button
      :labelName="'Another action'"
      :variant="'outline-dark'"
      :icon="'bookmarks'"
      :iconClass="'ml-2'"
      :size="'lmdg'"
      :setFunction="doSomething"
      :pill="false"
      :squared="false"
    />
  </div>
</template>

<script>
import Button from "./components/Button.vue";

export default {
  name: "App",
  components: {
    Button,
  },
  methods: {
    // Add function to use with a button
    sayHello() {
      alert("Say hello!");
    },
    sayBye() {
      alert("Say bye!");
    },
    doSomething() {
      console.log("Do something...");
    },
  },
};
</script>

<style>
</style>
