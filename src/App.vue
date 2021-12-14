<template>
  <div id="app">
    <!-- Navigation component -->
    <Navigation />

    <!-- Alerts -->
    <Button
      buttonText="Add warning alert"
      alertType="warning"
      alertMessage="Warning warning"

      @add-message="addAlert"
    />

    <Button
      buttonText="Add error alert"
      alertType="error"
      alertMessage="Omg an error occured"

      @handle-clicked="addAlert"
    />
    
    <Alert
      v-for="(error, index) in errors"
      :key="index"
      :message="error.message"
      :customClasses="error.customClasses"
    />

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
  // Components
  import Navigation from "./components/Navigation.vue";
  import Alert from "./components/Alert.vue";
  import Button from "./components/Button.vue";

  // Scss
  import style from "./scss/style.scss";

  // Export
  export default {
    name: 'App',
    data() {
      return {
        errors: [
        ],
      }
    },
    components: {
      Navigation,
      Alert,
      Button
    },
    methods: {
      addAlert(message, type) {
        this.errors.push({
            message: message,
            customClasses: type
          });
      }
    }
  }
</script>