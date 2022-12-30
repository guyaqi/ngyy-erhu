<script setup lang="ts">
// import { ref } from 'vue'

const nav = (index: number) => {
    if (index == 0) {
        return
    }

    let el = null
    if (index == 1) {
        el = document.querySelector('.info-2')
    }
    else if (index == 2) {
        el = document.querySelector('.info-4')
    }
    else {
        return
    }
    
    // console.log(el)
    const rect = el?.getBoundingClientRect()
    // console.log(rect)
    const y = rect?.top!!
    // console.log(y)
    window.scrollTo({
        top: y - 30,
        left: 0,
        behavior: 'smooth'
    })
}

</script>

<template>
  <div class="header">
    <div class="brand">
        <div class="main">横浜中華街二胡同好会</div>
        <div class="sub">横浜中華街二胡乐团</div>
    </div>
  </div>
  <div class="nav-bar">
    <div class="nav">
        <div @click="nav(0)" class="nav-item">首页</div>
        <div @click="nav(1)" class="nav-item">講師について</div>
        <div @click="nav(2)" class="nav-item">体験レッスン予約</div>
    </div>
    
  </div>
  <div class="disp">
    <img src="../assets/zhong_hua_jie.png" alt="">
  </div>
  <div class="info-1">
    <div class="align">
        <div class="table-like">
            <div class="table-head">レッスンについて / 课程介绍</div>
            <div class="table-item">ゼロから～（教材相談可）/ 歓迎初学者 教材非固定</div>
            <table class="table-inner">
                <tbody>
                    <tr>
                        <td>マンツーマン/１V１</td>
                        <td>グループA  ２人 / 两人小组课</td>
                        <td>グループB  ３人～６人/大组课 <br><span style="color: red">レベル近い　4人から開講</span></td>
                    </tr>
                    <tr>
                        <td>７０００円</td>
                        <td>４６００円 / 人</td>
                        <td>２５００円 / 人</td>
                    </tr>
                </tbody>
            </table>
            <div class="table-item">二胡楽団アンサンブル練習指導（二重奏・三重奏及び多人数楽団指導受付中）<br>
本会楽団団員募集中~二胡の上達に目指す～二胡のスキルを活かして楽しみに～<br>
申し込みはメールで～</div>
        </div>
        <div class="btn-apply">
            <div class="t" @click="nav(2)">申し込み</div>
            <img src="../assets/arrow.png" alt="" class="i">
        </div>
    </div>
  </div>
  <div class="info-2">
    <img class="teacher" src="../assets/jiang_shi.png" alt="">
    <div class="title"><span class="red">【</span> 講師紹介<span class="red">】</span></div>
    <div class="content">二胡演奏者<br>劉　晋陽 （リュウ　シンヨウ)<br><br>中国山西省出身。7歳から二胡を勉強し、2009年9月に天津音楽学院附属中学音楽学院に入学し、専攻は民族器楽演奏です。2012年9月に東北師範大学音楽学院に入学し、専攻は音楽学です。大学で音楽学理論、中国民族音楽、世界民族音楽、合唱指揮、民族管弦楽団の教育を受けました。同時期に、学校の管弦楽団の代表として、演奏活動で活躍した。そのほかに、二胡講師として、子供や大人など様々な年齢層の生徒を教えている。2016年10月に横浜国立大学の教育学部の研究生として入学し、2017年４月横浜国立大学の音楽教育の修士課程に入り、2019年３月で修了した。2019年4月から一年間は東京藝術大学の伝統音楽教育博士課程研究生として勉強したことがあり、それから神奈川県内小学校、中学校さらにマレーシアの華人小学校まで二胡と中国語・中国文化講座講師として活躍し、横浜と東京で沢山の演奏活動と教育活動を行われた。</div>
  </div>
  <div class="info-3">
    <div class="g">
        <div class="g1">横浜中華街馬さんの店<br>本店　龍仙　のとなり<br>双喜麺上海<br>Cafe & Shanghai pasta</div>
        <div class="g2">
            <div class="g21">
                <div class="g211">住所</div>
                <div class="g212">神奈川県横浜市中区山下町218-5</div>
            </div>
            <div class="g21">
                <div class="g211">アクセス</div>
                <div class="g212">JR根岸線「石川町」駅より徒歩 6分みなとみらい線「元町中華 街」駅から徒歩7分</div>
            </div>
        </div>
    </div>
    <div class="img-list">
        <img src="../assets/img_1.png" alt="">
        <img src="../assets/img_2.png" alt="">
        <img src="../assets/img_3.png" alt="">
    </div>
  </div>
  <div class="info-4">
    <div class="inner">
        無料体験レッスンやレッスン見学を希望するお客様は遠慮なくメールでご予約してください<br>
        <br>
        申し込み内容は<br>
        <br>
        お名前（漢字）：<br>
        お名前（カタカナ）：<br>
        連絡先：<br>
        体験レッスン/見学（一つ選択してください）：<br>
        予約したい時間帯：<br>
        （少なくても3つの日付と時間帯を参考候補として書いてください）<br>
        講師にコメント：<br>

        メール： <a href="mailto:nikonikoerhu@ymail.ne.jp">nikonikoerhu@ymail.ne.jp</a><br>
        みんなさんとの出会いを楽しみしております~<br>
    </div>
    
  </div>
  <div class="footer">
    <div class="g">
        <div class="g1">問い合わせ</div>
        <div class="g2">
            <div class="g21">メール: nikonikoerhu@ymail.ne.jp</div>
            <div class="g22">電話: 08043456688</div>
        </div>
        <div class="g3">
            <div class="g31">LINE: liujinyang123</div>
            <!-- <div class="g32">WeChat：</div> -->
        </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.header {
    max-width: 1320px;
    @media screen and (max-width: 1200px) {
        max-width: 980px;
    }
    margin: 0 auto;
    .brand {
        width: fit-content;
        padding: 0.5rem;
        .main {
            color: #a11f24;
            font-size: 2rem;
            margin: 0.5rem 0;
        }
        .sub {
            color: #a11f24;
            font-size: 1.25rem;
            text-align: right;
            margin-bottom: 0.5rem;
        }
        
    }
}

.nav-bar {
    height: 3rem;
    background-color: rgba(161, 31, 36, 88%);
    .nav {
        max-width: 1320px;
        @media screen and (max-width: 1200px) {
            max-width: 980px;
        }
        margin: 0 auto;
        display: flex; 
        overflow-x: scroll;
    }
    
    .nav-item {
        line-height: 3rem;
        color: white;
        margin: 0 0.5rem;
        padding: 0 0.5rem;
        transition: 0.25s;
        flex-shrink: 0;
        &:first-child {
            margin-left: 0rem;
        }
        &:hover {
            background-color: rgb(203, 30, 0);
            user-select: none;
            cursor: pointer;
        }
    }
}

.disp {
    img {
        width: 100%;
    }
}

.info-1 {
    background-image: url(../assets/bg_1.png);
    background-size: 100%;
    font-size: 1.25rem;
    @media screen and (max-width: 980px) {
        padding: 1rem;
    }

    .align {

        max-width: 578px;
        margin: 2rem auto;
    
        .table-like {
        
            .table-head {
                background-color: #a73437;
                color: #fff;
                // height: 2rem;
                line-height: 2rem;
                padding: 0.25rem 0.5rem;
                text-align: center;
            }
            table.table-inner {
                width: 100%;
                border-collapse:collapse;
                thead {

                }
                tbody {
                    td {
                        background-color: #e5e5e5;
                        border: 1px solid #aaaaaa;
                        padding: 0.25rem 0.5rem;
                        text-align: center;
                    }
                }
            }
            .table-item {
                // height: 2rem;
                line-height: 2rem;
                background-color: #e5e5e5;
                border: 1px solid #aaaaaa;
                padding: 0.25rem 0.5rem;
                text-align: center;
            }
        }
        .btn-apply {
            height: 2rem;
            width: fit-content;
            margin: 1rem 0;

            background-color: #a73437;
            padding: 0 1rem;
            
            align-items: center;
            justify-content: center;
            border-radius: 1rem;
            display: flex;
            align-items: center;

            user-select: none;
            cursor: pointer;

            .t {
                color: #fff;
            }
            img {
                height: 1.5rem;
                width: 1.5rem;
            }
        }
    }

    
}

.info-2 {
    max-width: 1320px;
    @media screen and (max-width: 1200px) {
        max-width: 980px;
    }
    display: flex;
    @media screen and (max-width: 980px) {
        flex-flow: column;
        align-items: center;
    }
    justify-content: center;
    margin: 5rem auto;
    .teacher {
        margin-right: 24px;
        max-width: 512px;
        flex-shrink: 0;
        width: 40%;
        object-fit: contain;
        @media screen and (max-width: 980px) {
            width: 80%;
        }
    }
    .title {
        font-size: 1.5rem;
        .red {
            color:#a11f24;
        }
        margin-right: 24px;
        writing-mode:vertical-lr;
        @media screen and (max-width: 980px) {
            writing-mode: horizontal-tb;
            margin-top: 1rem;
        }
    }
    .content {
        max-width: 578px;
        padding-top: 0.75rem;
        font-size: 1.25rem;
        @media screen and (max-width: 980px) {
            padding: 1rem;
        }
    }
}

.info-3 {
    max-width: 1320px;
    @media screen and (max-width: 1200px) {
        max-width: 980px;
    }
    @media screen and (max-width: 980px) {
        padding: 1rem;
    }
    
    margin: 2rem auto;
    .g {
        font-size: 1.25rem;
        display: flex;
        flex-flow: row wrap;
        align-items: flex-end;
        margin: 0 auto;
        margin-bottom: 2rem;

        
        
        .g1 {
            background-color: #a11f24;
            color: #fff;
            white-space: nowrap;
            line-height: 2rem;
            padding: 1rem;
            
            // @media screen and (max-width: 980px) {
            //     width: 100%;
            // }
        }
        .g2 {
            
            >div {
                display: flex;
                &>div {
                    background-color: #e5e5e5;
                    border: 1px solid #aaaaaa;
                    padding: 0.5rem;
                    
                    &:nth-child(1) {
                        width: 120px;
                        flex-shrink: 0;
                    }
                    &:nth-child(2) {
                        flex-grow: 1;
                    }
                }
            }
        }
        .g3 {
            flex-grow: 1;
        }
    }

    .img-list {
        display: flex;
        justify-content: space-between;
        width: 100%;
        @media screen and (max-width: 980px) {
            flex-flow: column;
        }
        >img {
            display: block;
            width: 32%;
            @media screen and (max-width: 980px) {
                width: 100%;
                margin-bottom: 1rem;
            }
        }
    }
}

.info-4 {
    
    padding: 15px;
    // white-space: pre-line;
    // word-break: break-all;
    // word-wrap: break-word;

    max-width: 1320px;
    @media screen and (max-width: 1200px) {
        max-width: 980px;
    }
    @media screen and (max-width: 980px) {
        padding: 1rem;
    }
    
    margin: 2rem auto;

    font-size: 1.25rem;

    .inner {
        border: 2rem solid #e1e4f3;
        background-color: #fff;
        padding: 2rem;
    }
}

.footer {
    background-color: #a11f24;
    @media screen and (max-width: 980px) {
        padding: 1rem;
    }
    .g {
        max-width: 1320px;
        margin: 0 auto;
        padding: 1rem 0;
        color: #fff;
        line-height: 1.5rem;
        
        .g1 {
            font-size: 1.25rem;
            margin-bottom: 0.25rem;
        }
    }
}
</style>
