<template>
    <section id="application-domain" class="content-container application-domain content-container">
        <div class="section-main-title">產業實際應用</div>
        <el-row
            v-for="(item, index) in items"
            :key="index"
            type="flex"
            align="middle"
            class="application-domain--domain"
        >
            <el-col :span="12" class="application-domain--image">
                <el-row type="flex" justify="start" class="img-wrapper">
                    <el-image fit="contain" :src="item.image" v-if="item.image.length" />
                </el-row>
            </el-col>
            <el-col :span="12" class="application-domain--paragraph">
                <div>
                    <el-row type="flex" align="middle" justify="center">
                        <el-col :span="12">
                            <el-row type="flex" justify="start" class="img-wrapper fit-height">
                                <el-image class="applicatino-domain--thumbnail" fit="contain" :src="item.thumbnail" />
                            </el-row>
                        </el-col>
                        <el-col :span="12"><h3>{{ item.title }}</h3></el-col>
                    </el-row>
                </div>
                <div>
                   {{ item.desc }} 
                </div>
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
                    image: '/statics/images/application-manufacture.gif',
                    thumbnail: '/statics/images/application-manufacture-s.gif',
                    title: '製造業',
                    desc: 'AI取代人力，迴避因疲乏出錯。達到更快速，更精準檢測。',
                },
                {
                    image: '/statics/images/application-traffic.gif',
                    thumbnail: '/statics/images/application-traffic-s.gif',
                    title: '交通',
                    desc: '及時辨識路況，輔助行車安全。',
                },
                {
                    image: '/statics/images/application-produce.gif',
                    thumbnail: '/statics/images/application-produce-s.png',
                    title: '農漁業',
                    desc: '運用AOI，快速篩選分類農產品',
                },
                {
                    image: '',
                    thumbnail: '/statics/images/application-medical-s.png',
                    title: '生技醫療',
                    desc: '',
                },
                {
                    image: '/statics/images/application-disaster.png',
                    thumbnail: '/statics/images/application-disaster-s.gif',
                    title: '災害預警',
                    desc: '',
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
    .application-domain--paragraph {
        padding: 16px 18px;

        @media @for-size-md {
            padding: 18px 24px;
        }
    }

    .application-domain--image {
        padding-left: 8px;
        padding-right: 8px;

        @media @for-size-md {
            padding-left: 16px;
            padding-right: 16px;
        }
    }


    .img-wrapper {
        min-height: 170px;
        width: 100%;
        margin-bottom: 4px;
        overflow: hidden;

        &.fit-height {
            padding: 8px;
            min-height: 0;
            height: auto;
        }

        &:nth-child(2n) {
            margin-left: 18px;
        }

        img, .el-image {
            width: 100%;
            height: 100%;
        }
    }
}
</style>
