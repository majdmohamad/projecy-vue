<template>
    <div class="our-blog">
        <h1>{{ pageName }}</h1>
        <p>{{ pageDescription }}</p>
        <div class="container">
            <div class="row">
                <div class="col-md-8">
                    <div class="posts-area">
                        <BlogPosts
                            v-for="post in posts"
                            v-bind:key="post.id"
                            :viewe="post.viewe"
                            :title="post.title"
                            :content="post.content"
                            :author="post.author"
                            :category="post.category"
                        />
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="sidebar">
                        <BlogSidebar />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import BlogPosts from "@/components/BlogPosts.vue";
import BlogSidebar from "@/components/BlogSidebar.vue";
import JsonPosts from "../json/blog-posts.json";

export default {
    data: function () {
        return {
            pageName: "Blog",
            pageDescription: "This Is Blog Page",
            posts: JsonPosts,
        };
    },
    name: "blogMy",
    components: {
        BlogPosts,
        BlogSidebar,
    },
};
</script>
