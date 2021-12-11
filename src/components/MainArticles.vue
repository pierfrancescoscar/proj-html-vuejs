<template>
  <section class="container-fluid p-5">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <nav>
            <ul class="d-flex flex-wrap ps-0">
              <li
                class="col-4 list-unstyled pe-4"
                v-for="(post, index) in articles"
                :key="`article-${index}`"
              >
                <div>
                  <img
                    class="img-fluid"
                    :src="require(`@/assets/${post.image}.jpg`)"
                    :alt="post.text"
                  />

                  <div class="post-content p-3">
                    <div class="category-tag pb-3">
                      <span class="text-white text-uppercase p-2 rounded">
                        {{ post.category }}
                      </span>
                    </div>
                    <div class="post-title">
                      <a
                        class="text-decoration-none text-white"
                        :href="post.url"
                        >{{ post.text }}</a
                      >

                      <div class="hover-text">
                        <a
                          class="text-decoration-none addictional-text"
                          href="#"
                        >
                          Lorem ipsum dolor, sit amet consectetur adipisicing
                          elit. Voluptatem dolore, quia eaque veniam quibusdam
                          voluptates optio voluptas fugit possimus, deleniti
                          cumque!
                        </a>
                      </div>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "MainArticles",
  props: {
    articles: Array,
  },
};
</script>

<style scoped lang="scss">
@import "@/style/vars.scss";

section {
  background-color: $background-2;
}

li {
  position: relative;
  cursor: pointer;
  &:hover img {
    filter: brightness(0.4);
  }
}

img {
  transition: filter 0.4s linear;
}

span {
  font-weight: $medium-fw;
  font-size: $minor-fs;
  background-color: $background-4;
}

a {
  font-size: $big-fs;
  font-weight: $extrastrong-fw;
}

li:nth-child(1),
li:nth-child(2),
li:nth-child(3) {
  margin-bottom: 1.5rem;
}

.post-content {
  position: absolute;
  bottom: 20px;
  left: 0px;
  right: 20px;
}

.addictional-text {
  display: none;
  font-size: $minor-fs;
  color: $text-5;
  font-weight: $strong-fw;
  
}

li:hover .addictional-text {
  display: block;

}
</style>
