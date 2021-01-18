<template>
    <div class="container">
        <Header></Header>
        <About></About>
        <CSR></CSR>
        <ApplicationDomain></ApplicationDomain>
        <FAQ></FAQ>
        <ContactUs></ContactUs>
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

.container {
    margin: 0 auto;
    max-width: 1440px;

    .content-container {
        padding-left: 14px;
        padding-right: 14px;
    }
}
</style>
