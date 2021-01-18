<template>
    <NuxtLink
        :to="{ path: item.path, hash: item.hash }"
        :class="{ active: isActive }"
        class="top-nav-menu-item"
        >{{ item.label }}</NuxtLink
    >
</template>

<script>
export default {
    props: {
        item: {
            type: Object,
            default: () => ({}),
        },
    },

    data() {
        return {
            isActive:
                this.$route.path.split('/')[1].toString() ===
                this.item.path.split('/')[1].toString(),
        }
    },

    watch: {
        $route(to, from) {
            this.isActive =
                to.path.split('/')[1].toString() ===
                this.item.path.split('/')[1].toString()
        },
    },
}
</script>

<style lang="less" scoped>
.top-nav-menu-item {
    padding: 16px 18px;
    text-decoration: none;
    color: #fff;
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 30px;

    &:hover {
        background-color: #2f6e21;
    }
}
</style>
