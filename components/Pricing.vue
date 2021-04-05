<template>
    <section class="content-container section-pricing">
        <div class="section-main-title">圖資標記估價</div>
        <div class="section-main-content">
            <el-row type="flex" align="middle" justify="center" class="flex-wrap">
                <div
                    v-for="item in categories"
                    :key="item.key"
                    class="pricing--category">
                    <div class="pricing--title">{{ item.title }}</div>
                    <div class="pricing--price">{{ item.price }}</div>
                    <div>張數：{{ item.quantity }}張</div>
                    <div>單價：{{ item.unit }}∕孔</div>
                    <div>設定費：{{ item.fee }}</div>
                    <div>公式:</div>
                    <div>圖張數+(圖張數*孔數)+設定費</div>
                </div>
            </el-row>
        </div>
    </section>
</template>

<style lang="less" scoped>
.section-pricing {
    .pricing--category {
        margin-bottom: 48px;
        width: 360px;
        .font-size--title-md();
        text-align: center;

        .pricing--title {
            .font-size--title-md-strong();
        }

        .pricing--price {
            .font-size--display();
        }
    }
}

</style>

<script>
export default {
    data() {
        return {
            categories: [
                {
                    key: 'plan A',
                    title: '方案 A',
                    price: '$5,000+',
                    quantity: '1-200',
                    unit: '68.35',
                    fee: '$5,000',
                },
                {
                    key: 'plan B',
                    title: '方案 B',
                    price: '$12,000+',
                    quantity: '201-700',
                    unit: '68.35',
                    fee: '$12,000',
                },
                {
                    key: 'plan C',
                    title: '方案 C',
                    price: '$15,000+',
                    quantity: '701-1000',
                    unit: '68.35',
                    fee: '$15,000',
                },
                {
                    key: 'plan D',
                    title: '方案 D',
                    price: '$20,000+',
                    quantity: '1001-1500',
                    unit: '68.35',
                    fee: '$20,000',
                },
            ]
        };
    },
}
</script>