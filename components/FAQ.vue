<template>
    <section id="faq" class="section content-container">
        <h2 class="section-title">常見問題</h2>
        <div v-for="(item, index) in qna" :key="index" class="qa-item">
            <h3>{{ index + 1 }}.{{ item.title }}</h3>
            <span>{{ item.desc }}</span>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            qna: [
                {
                    title: '不知道要使用什麼標註方式來定義數據？',
                    desc:
                        '與專業AI工程師進行討論，以經驗判斷來說明並給予建議。不同圖資需要不同的標註工具來標註。',
                },
                {
                    title: '標註數據圖資需要多少量才適合？',
                    desc:
                        '取決於數據圖資是否完整、清楚、有無雜訊，精確的圖資是最適合用來訓練模型，當然量越多精準度越高。',
                },
                {
                    title: '需標註的圖資如何估價？',
                    desc: '可以參考振海資通網頁上的商品服務估價的內容明細。',
                },
                {
                    title: '自己請工讀生或找兼職會比較省成本嗎？',
                    desc:
                        '找工讀生或找兼職需要花費時間和成本，加上公司需要給予勞健保費，且工讀生及兼職都不是很穩定，隨時都可能離職，對於很急需的圖資標註很難有好的品質，想要用低廉的成本聘請，反而勞心勞力。',
                },
                {
                    title: '簽約後大概多久可以交貨？',
                    desc: '簽訂買賣合同後，會在一週內擬定交件數量與交件週期。',
                },
                {
                    title: '如果驗收過後又發現有問題可以再修改嗎？',
                    desc:
                        '在收貨後十四日內進行驗收及回覆賣方驗收結果，超出期限者得視為買方完成通過驗收。',
                },
                {
                    title: '標註圖資是否有免費的工具使用？',
                    desc:
                        '網路上搜尋可找到IBM的Cloud Annotations自動化標註工具  、微軟Azure的Visual Object Tagging Tool、AWS的Amazon Rekognition自訂標籤 、LabelImg 免費的影像標註工具 都是可以參考使用。',
                },
            ],
        }
    },
}
</script>

<style lang="less" scoped>
#faq {
    .qa-item {
        margin-bottom: 18px;
    }
}
</style>
