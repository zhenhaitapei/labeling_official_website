<template>
    <section id="application-domain" class="section content-container">
        <h2 class="section-title">AI領域應用</h2>
        <el-row
            v-for="(item, index) in items"
            :key="index"
            type="flex"
            align="middle"
            class="application-domain--domain"
            :class="{ reverse: index % 2 > 0 }"
        >
            <el-col :span="14">
                <h3>{{ item.title }}</h3>
                <ol>
                    <li v-for="(des, idx) in item.desc" :key="idx">
                        <span>{{ des }}</span>
                    </li>
                </ol>
            </el-col>
            <el-col :span="10">
                <el-row type="flex" justify="start" class="img-wrapper">
                    <el-image fit="contain" :src="item.image" />
                </el-row>
            </el-col>
        </el-row>
    </section>
</template>

<script>
export default {
    data() {
        return {
            items: [
                {
                    image: require('~/assets/images/domain1.png'),
                    title: '製造業',
                    desc: [
                        '預警系統減少停機損失',
                        '提高產品良率',
                        '節省人力成本',
                        '安全的廠域',
                        '趨勢預測快速決策',
                    ],
                },
                {
                    image: require('~/assets/images/domain2.jpg'),
                    title: '交通(車輛標註)',
                    desc: [
                        '辨識及追蹤交通工具',
                        '事件告警',
                        '即時路況資訊',
                        '增進自駕車運行安全',
                        '道路建設規劃',
                    ],
                },
                {
                    image: require('~/assets/images/domain3.gif'),
                    title: '手勢辨識',
                    desc: [
                        '幫助手語及口語族群相互溝通',
                        '線上體感遊戲及遙控器裝置使用',
                        '電視數位機上盒使用',
                        '體感健身活動使用',
                        '數位互動教學',
                    ],
                },
                {
                    image: require('~/assets/images/domain4.jpg'),
                    title: '災害預警',
                    desc: [
                        '預測地震、土石流等自然災害',
                        '提早進行災害管理及資源配置',
                        '減少人員傷害',
                        '機器學習協助救災',
                    ],
                },
                {
                    image: require('~/assets/images/domain5.jpg'),
                    title: '農漁業 ',
                    desc: [
                        '解決人力問題',
                        '監測溫度、濕度、肥料(飼料)',
                        '監測植物生長狀況',
                        '節省水電、農藥(藥物)、花費的消耗',
                        '監測動物健康及生長情形',
                    ],
                },
            ],
        }
    },
    computed: {
        doImage(fileName) {
            return require(`~/assets/images/${fileName}`)
        },
    },
}
</script>

<style lang="less" scoped>
#application-domain {
    .application-domain--domain {
        margin-bottom: 18px;

        &.reverse {
            flex-direction: row-reverse;
        }
    }

    .img-wrapper {
        height: 250px;
        width: 40%;
        margin-bottom: 4px;
        overflow: hidden;

        &:nth-child(2n) {
            margin-left: 18px;
        }

        img {
            width: 100%;
            height: 100%;
        }
    }
}
</style>
