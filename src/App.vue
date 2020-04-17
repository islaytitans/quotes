<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <button @click="selectedComponent = 'appQuote'">Quote</button>
        <button @click="selectedComponent = 'appAuthor'">Author</button>
        <button @click="selectedComponent = 'appNew'">New</button>
        <hr />
        <keep-alive>
          <component :is="selectedComponent">
            <p>Default content</p>
          </component>
        </keep-alive>
        <!-- <component :is="selectedComponent">
          <p>Default content</p>
        </component> -->
      </div>
    </div>
  </div>
</template>

<script>
import Quote from "./components/Quote.vue";
import New from "./components/New.vue";
import Author from "./components/Author.vue";

export default {
  data() {
    return {
      quoteTitle: "The Quote",
      selectedComponent: "app-quote",
    };
  },
  components: {
    appQuote: Quote,
    appAuthor: Author,
    appNew: New,
  },
};
</script>

<style></style>
