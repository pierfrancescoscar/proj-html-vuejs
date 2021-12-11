<template>
  <section class="container-fluid p-5">
    <div class="container">
      <div class="row">
        <div class="col-4">
          <h3 class="text-uppercase">Popular Posts</h3>
          <nav>
            <ul class="ps-0">
              <li
                class="list-unstyled d-flex mb-3 mt-3"
                v-for="(link, index) in popular"
                :key="`article-${index}`"
              >
                <img
                  class="post-img img-fluid me-3 mb-3"
                  :src="require(`@/assets/${link.image}.jpg`)"
                  :alt="link.text"
                />

                <div class="link-content">
                  <div class="link-title">
                    <a class="text-decoration-none" :href="link.url">{{
                      link.text
                    }}</a>
                  </div>

                  <div class="link-date">
                    <span>{{ link.date }}</span>
                  </div>
                </div>
              </li>
            </ul>
          </nav>
        </div>
        <div class="col-4">
          <h3 class="text-uppercase">Recent Posts</h3>
          <nav>
            <ul class="ps-0">
              <li
                class="list-unstyled d-flex mb-3 mt-3"
                v-for="(link, index) in recent"
                :key="`article-${index}`"
              >
                <img
                  class="post-img img-fluid me-3 mb-3"
                  :src="require(`@/assets/${link.image}.jpg`)"
                  :alt="link.text"
                />

                <div class="link-content">
                  <div class="link-title">
                    <a class="text-decoration-none" :href="link.url">{{
                      link.text
                    }}</a>
                  </div>

                  <div class="link-date">
                    <span>{{ link.date }}</span>
                  </div>
                </div>
              </li>
            </ul>
          </nav>
        </div>
        <div class="col-4">
          <h3 class="text-uppercase mb-4">Featured Posts</h3>
          <div class="post-card">
            <img
              class="img-fluid"
              src="../assets/blog-66.jpg"
              alt="recipies-article"
            />

            <div class="post-content p-3">
              <div class="category-tag pb-3">
                <span class="category text-white text-uppercase p-2 rounded">
                  Recipies
                </span>
              </div>
              <div class="post-title">
                <a
                  class="article-title text-decoration-none text-white"
                  href="#"
                  >Tips To Help You Quickly prepare Your Lunch</a
                >
              </div>

              <div class="hover-text">
                        <a
                          class="text-decoration-none addictional-text"
                          href="#"
                        >
                          Lorem ipsum dolor, sit amet consectetur adipisicing
                          elit.
                        </a>
                </div>

            </div>
          </div>
          <h3 class="text-uppercase mt-4 mb-3">Featured Author</h3>
          <div class="author-content d-flex">
            <img
              class="avatar img-fluid"
              src="../assets/avatar.jpg"
              alt="author-avatar"
            />
            <div class="ps-3 author-text">
              <h3 class="pt-2 author-name">John Doe</h3>
              <span
                >Lorem ipsum dolor sit amet, consectur adiscipling elit. Nam
                viverra euismod odio, gravida pelle, consectur adiscipling elit.
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "PostList",
  props: {
    popular: Array,
    recent: Array,
  },
};
</script>

<style scoped lang="scss">
@import "@/style/vars.scss";

section {
  background-color: $background-1;
}
h3 {
  color: $text-7;
  font-weight: $strong-fw;
  font-size: $medium-fs;
}

li {
  border-bottom: 1px dashed $text-3;
}

.post-img {
  width: 50px;
  height: 50px;
  object-fit: cover;
}

a {
  font-size: $medium-fs;
  color: $text-9;
}

span {
  font-size: $minor-fs;
  color: $text-3;
}

.post-card {
  position: relative;
}

.post-content {
  position: absolute;
  bottom: 20px;
  left: 0px;
  right: 20px;
}
.category {
  font-weight: $medium-fw;
  font-size: $minor-fs;
  background-color: $background-4;
}

.post-title {
  font-size: $medium-fs;
  font-weight: $extrastrong-fw;
}

.article-title {
  font-size: $big-fs;
}

.avatar {
  width: 160px;
  height: 160px;
  object-fit: cover;
}

.author-name {
  font-size: $semibig-fs;
  font-weight: $strong-fw;
}

.addictional-text {
  display: none;
  font-size: $minor-fs;
  color: $text-5;
  font-weight: $strong-fw;
  
}

.post-card:hover .addictional-text {
  display: block;

}

.post-card {
    &:hover img {
    filter: brightness(0.4);
  }
}

img {
    transition: filter 0.4s linear;

}
</style>
