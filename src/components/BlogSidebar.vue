<template>
    <div class="side-box">
        <h2 class="side-title">New Post</h2>
        <div class="box-content">
            <p>
                <input type="text" placeholder="Author name" name="username" />
            </p>
            <p><input type="text" placeholder="title" name="subject" /></p>
            <p><input type="email" placeholder="category" name="subject" /></p>
            <textarea name="article" placeholder="your Post"></textarea>
            <p><input type="submit" value="Send" /></p>
        </div>
    </div>
</template>

<script>
export default {
    name: "blog-sidebar",
};
</script>

<style lang="scss" scoped>
.side-box {
    padding: 20px;
    height: 800px;
    background-color: #fff;
    box-shadow: 0 0 10px #ddd;
    position: relative;
    .side-title {
        position: absolute;
        top: 5px;
        left: 5px;
        background-color: #4caf50;
        border-radius: 4px;
        padding: 1px 5px;
        color: #fff;
        text-align: center;
        font-weight: bold;
    }
    .box-content {
        position: absolute;
        top: 50px;
        left: 5px;
    }
    textarea {
        width: 400px;
        height: 400px;
    }
}
</style>
