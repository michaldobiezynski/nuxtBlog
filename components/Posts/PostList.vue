<template>
  <section class="featured-posts">
    <PostPreview
      id="1"
      title="Hello there"
      previewText="This is my first post!"
      thumbnail="https://imageio.forbes.com/specials-images/imageserve/61d52d4e3a76ed81ac034ea8/The-10-Tech-Trends-That-Will-Transform-Our-World/960x0.jpg?fit=bounds&format=jpg&width=960"
    />
    <PostPreview
      id="2"
      title="Hello there 2"
      previewText="This is my second post!"
      thumbnail="https://imageio.forbes.com/specials-images/imageserve/61d52d4e3a76ed81ac034ea8/The-10-Tech-Trends-That-Will-Transform-Our-World/960x0.jpg?fit=bounds&format=jpg&width=960"
    />
    <PostPreview
      id="3"
      title="Hi"
      previewText="This is my third post!"
      thumbnail="https://imageio.forbes.com/specials-images/imageserve/61d52d4e3a76ed81ac034ea8/The-10-Tech-Trends-That-Will-Transform-Our-World/960x0.jpg?fit=bounds&format=jpg&width=960"
    />
  </section>
</template>

<script>
import PostPreview from "@/components/Posts/PostPreview";

export default {
  components: { PostPreview },
};
</script>

<style scope>


.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>