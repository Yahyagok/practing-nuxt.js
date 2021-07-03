<template>
  <div>
    <h3>Customer Reviews</h3>
    <div>
       <ReviewCard 
        v-for="reviewer in reviewers.results"
        :key="reviewer.login.uui"
        :review= "reviewer"
       />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reviewers: []
    };
  },
  async fetch() {
    this.reviewers = await fetch('https://randomuser.me/api/?results=5').then(res =>
      res.json()
    );
  }
};
</script>

<style scoped></style>
