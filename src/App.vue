<template>
  <div id="app">
    <!-- Navigation component -->
    <nav class="c-nav">
      <ul class="c-nav-list">
        <li class="c-nav-list-item active">
          Home
        </li>

        <li class="c-nav-list-item">
          Voting
        </li>
      </ul>
    </nav>

    <!-- Alerts -->
    <div class="c-alert">
      Woops something went wrong
    </div>

    <div class="c-alert warning">
      Warning warning, you should pay attention
    </div>

    <div class="c-alert succes">
      Great Success
    </div>

    <div class="c-alert neutral">
      Great Success
    </div>

    <!-- Main content -->
    <h1>
      Eurosong festival
    </h1>

    <p>
      This is our voting application
    </p>

  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import style from "./scss/style.scss";

  export default {
    name: 'App',
    components: {
      HelloWorld
    }
  }
</script>