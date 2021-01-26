<template>
    <section id="csr" class="section content-container">
        <h2 class="section-title">社會企業責任</h2>
        <el-row type="flex" align="middle">
            <div class="">
                <el-row type="flex" justify="start" class="img-wrapper">
                    <img src="~/assets/images/csr1.png" />
                </el-row>
                <el-row type="flex" justify="end" class="img-wrapper">
                    <img src="~/assets/images/csr2.jpg" />
                </el-row>
                <el-row type="flex" justify="start" class="img-wrapper">
                    <img src="~/assets/images/csr3.jpg" />
                </el-row>
            </div>
            <ol>
                <li
                    v-for="(item, index) in items"
                    :key="index"
                    class="csr-item"
                >
                    <span>{{ item.desc }}</span>
                </li>
            </ol>
        </el-row>
    </section>
</template>

<script>
export default {
    data() {
        return {
            items: [
                {
                    desc:
                        '訓練聽損者工作技能，適材適用，與社會公益機構合作，將社會資源有效運用，讓聽損者真正實踐獨立自主生活。',
                },
                {
                    desc:
                        '為聽損者創立居家工作機會，透過遠距訓練及視訊溝通，達到溝通無障礙的工作型態。',
                },
                {
                    desc:
                        '運用貼心的職務再設計，使用溝通輔具，調整工作方法由難到簡，實踐有效率、無壓力的工作環境。',
                },
            ],
        }
    },
}
</script>

<style lang="less" scoped>
#csr {
    .csr-item {
        margin-bottom: 14px;
    }

    .img-wrapper {
        width: 110px;
        height: 52px;
        margin-bottom: 4px;
        overflow: hidden;

        &:nth-child(2n) {
            margin-left: 24px;
        }

        @media @for-size-md {
        height: 104px;
        width: 220px;

        &:nth-child(2n) {
            margin-left: 44px;
        }

        }

        img {
            object-fit: contain;
        }
    }
}
</style>
