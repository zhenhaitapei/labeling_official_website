<template>
    <div class="container">
        <Header></Header>
        <div class="hero-image"></div>
        <About></About>
        <Products></Products>
        <Pricing></Pricing>
        <WorkFlow></WorkFlow>
        <ApplicationDomain></ApplicationDomain>
        <CSR></CSR>
        <FAQ></FAQ>
    </div>
</template>

<script>
export default {}
</script>

<style lang="less">
html {
    font-family: 'Helvetica Neue', Helvetica, 'PingFang SC', 'Hiragino Sans GB',
        'Microsoft YaHei', '微软雅黑', Arial, sans-serif;
    font-size: 14px;
    color: #2f495e;

    body {
        margin: 0;
        min-width: 360px;
    }

    * {
        box-sizing: border-box;
    }
}

.hero-image {
    background-image: url("~static/statics/images/hero-image.png");

    min-height: 80vh;
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

.container {
    .content-container {
        margin: 0 auto;
        max-width: 768px;
        padding: 14px 0 40px;
    }
}
</style>
