<template>
    <div class="header">
        <div class="header-content">
        <el-row type="flex" align="bottom">
            <div class="logo">ZHAI LABHUB</div>
        </el-row>
        </div>
    </div>
</template>

<style lang="less" scoped>
.header {
    background: #fff;
    z-index: 9;
    position: sticky;
    top: 0;
    border-bottom: solid 1px #70a2d6;

    .header-content {
        max-width: 1440px;
        margin: 0 auto;
    }

    .logo {
        font-size: 36px;
        background: linear-gradient(to right, #1a68b1, #70a2d6, #16338c);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        padding: 12px 8px;

        @media only screen and (min-width: 768px) {
            font-size: 64px;
            padding: 14px 12px;
        }
    }
}
</style>
