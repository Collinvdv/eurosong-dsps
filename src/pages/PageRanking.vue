<template>
    <div>
      <button @click="changePage('home')">
        Go back to home
      </button>

      Ranking
    </div>
</template>

<script>
    export default {
        name: "PageRanking",
        methods: {
            changePage(page) {
                this.$emit("change-page", page);
            }
        }
    }
</script>