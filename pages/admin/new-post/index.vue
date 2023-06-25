<template>
  <div class="admin-new-post-page">
    <section class="new-post-form">
      <AdminPostForm @submit="onSubmitted" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from "@/components/Admin/AdminPostForm";
import axios from "axios";

export default {
  layout: "admin",

  components: { AdminPostForm },
  methods: {
    onSubmitted(formData) {
      axios
        .post(
          "https://nuxt-blog-25e9f-default-rtdb.europe-west1.firebasedatabase.app/posts.json",
          { ...formData, updatedDate: new Date() }
        )
        .then(() => this.$router.push("/posts"))
        .catch((e) => console.error(e));
    },
  },
};
</script>

<style scoped>
.new-post-form {
  width: 90%;
  margin: 20px auto;
}

@media (min-width: 768px) {
  .new-post-form {
    width: 500px;
  }
}
</style>
