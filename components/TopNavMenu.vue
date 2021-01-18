<template>
    <div class="top-nav-menu">
        <el-row type="flex" justify="end" align="middle">
            <TopNavMenuItem
                v-for="item in menu"
                :key="item.path + item.hash"
                :item="item"
            />
        </el-row>
    </div>
</template>

<script>
export default {
    data() {
        return {
            menu: [
                {
                    label: '首頁',
                    path: '/',
                    hash: '#main',
                },
                {
                    label: '商品服務',
                    path: '/',
                    hash: '#products',
                },
                {
                    label: '社會企業責任',
                    path: '/',
                    hash: '#csr',
                },
                {
                    label: '常見問題',
                    path: '/',
                    hash: '#faq',
                },
            ],
        }
    },
}
</script>
