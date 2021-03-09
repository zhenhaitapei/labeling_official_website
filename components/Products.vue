<template>
    <section class="content-container section-products">
        <div class="section-main-title">服務項目</div>
        <div class="section-desc">
            <div class="product--category">
                <div class="product--title">
                    Semantic Segmentation(語義分割)
                </div>
                <el-row type="flex" class="product--content">
                    <div class="product--desc">
                        <span>對每個需要的圖像賦予不同標籤，標記出不同顏色的像素。標註一個物件需較為耗時。</span><br><br>
                        <strong>標註注意事項：</strong><br>
                        <span>先描繪線條輪廓，然後倒入顏色，標註需判別輪廓邊線，容許值在1-2象素。</span><br><br>
                        <strong>適用於：</strong><br>
                        <ul>
                            <li>任何可見的物件</li>
                        </ul>
                    </div>
                    <div class="product-image">
                        <img src="/statics/images/e88ab1e793a3_gif-1-1.gif" alt="語義分割標記">
                        <div class="text-center">語義分割標記</div>

                    </div>
                </el-row>
            </div>
            <div class="product--category">
                <div class="product--title">
                    Image Classification(影像分類)
                </div>
                <el-row type="flex" class="product--content">
                    <div class="product--desc">
                        <span>圖資在在標註前需進行規範及定義，將圖資有系統分類，便於標註師快速精確標註，也可建立一個由自己所挑選圖像的分類模型。</span><br><br>
                        <strong>分類注意事項：</strong><br>
                        <span>由於圖資數量大，需要快速且精確分類，分類者需要有專業知識。</span><br><br>
                        <strong>適用於：</strong><br>
                        <ul>
                            <li>大量用於相似的動物和植物。</li>
                            <li>建置龐大的數據</li>
                        </ul>
                    </div>
                    <div class="product-image">
                        <img src="/statics/images/image-classification.gif" alt="檔案資料庫建設">
                        <div class="text-center">檔案資料庫建設</div>

                    </div>
                </el-row>
            </div>
            <div class="product--category">
                <div class="product--title">
                    Bounding Box(定界框)
                </div>
                <el-row type="flex" class="product--content">
                    <div class="product--desc">
                        <span>利用標記工具框出矩形邊界，快速框出選取區域，一個方框的速度約略2-3秒。</span><br><br>
                        <strong>標註注意事項：</strong><br>
                        <span>標註框需貼著物件邊線標註</span><br><br>
                        <strong>適用於：</strong><br>
                        <ul>
                            <li>形狀統一的物件</li>
                            <li>物件不要重疊，需要能算出的物件</li>
                        </ul>
                    </div>
                    <div class="product-image">
                        <img src="/statics/images/bounding-box.gif" alt="文字邊界框">
                        <div class="text-center">文字邊界框</div>

                    </div>
                </el-row>
            </div>
            <div class="product--category">
                <div class="product--title">
                    Polygon(多邊形標註)
                </div>
                <el-row type="flex" class="product--content">
                    <div class="product--desc">
                        <span>在物件的輪廓標記出不同的點，然後點與點間拉出一個線，標註一物件較為耗時。</span><br><br>
                        <strong>標註注意事項：</strong><br>
                        <span>點與線條需貼著物件的邊線標註。</span><br><br>
                        <strong>適用於：</strong><br>
                        <ul>
                            <li>任何可見的物體</li>
                        </ul>
                    </div>
                    <div class="product-image">
                        <img src="/statics/images/polygon.gif" alt="polygon">
                    </div>
                </el-row>
            </div>
            <div class="product--category">
                <div class="product--title">
                    Hand Tracking and Gesture Recognition(手勢追蹤及辨識)
                </div>
                <el-row type="flex" class="product--content">
                    <div class="product--desc">
                        <span>標註在動態的相同關鍵點，快速點選拉線。</span><br><br>
                        <strong>標註注意事項：</strong><br>
                        <span>需精確在關鍵點標註，隨著動態圖資標註相同的節點上。</span><br><br>
                        <strong>適用於：</strong><br>
                        <ul>
                            <li>非接觸式感應物件，因疫情期間衛生相對重要。</li>
                            <li>遊戲機</li>
                            <li>關節數量確定的對象<br>如：手語識別 </li>
                        </ul>
                    </div>
                    <div class="product-image" style="text-align: center;">
                        <img src="/statics/images/gesture.gif" alt="手勢追蹤及辨識" style="border-radius: 9999px; max-width: 300px;">
                    </div>
                </el-row>
            </div>
            <div class="product--category">
                <div class="product--title">
                    Line of Position(定位線)
                </div>
                <el-row type="flex" class="product--content">
                    <div class="product--desc">
                        <span>依據規範和定義，快速拉出一條線，速度約略2-3秒。</span><br><br>
                        <strong>標註注意事項：</strong><br>
                        <span>線條需貼著物件的邊線標註</span><br><br>
                        <strong>適用於：</strong><br>
                        <ul>
                            <li>需要追踪且重要的數據庫。</li>
                        </ul>
                    </div>
                    <div class="product-image">
                        <img src="/statics/images/line-of-position.gif" alt="定位線">
                    </div>
                </el-row>
            </div>
        </div>
    </section>
</template>

<style lang="less" scoped>
.section-products {
    .product--category {
        margin-bottom: 48px;
    }
    .product--title {
        font-style: normal;
        font-weight: bold;
        font-size: 22px;
        line-height: 1.4;
        margin-bottom: 16px;
    }
    .product--desc {
        width: 40%;
    }
    .product-image {
        padding-left: 24px;
        width: 60%;
        img {
            width: 100%;
        }
    }
}

</style>
