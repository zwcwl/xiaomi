<template>
    <div class="home-hero">
        <div class="home-swiper">
            <ul>
                <li><a href=""><img src="" alt=""></a></li>
                <li><a href=""><img src="" alt=""></a></li>
                <li><a href=""><img src="" alt=""></a></li>
                <li><a href=""><img src="" alt=""></a></li>
            </ul>
            <div class="btn-rl">
                <button class="btn-left"><i class="iconfont icon-back"></i></button>
                <button class="btn-right"><i class="iconfont icon-back"></i></button>
            </div>
            <div class="btn-pagination">
                <a href=""></a>
                <a href=""></a>
                <a href=""></a>
                <a href=""></a>
                <a href=""></a>
            </div>
        </div>

        <div class="home-list">
            <ul>
                <li><a href=""><span>Xiaomi手机</span></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
            </ul>
        </div>

        <div class="home-sub clearfix">
            <div class="home-channel-list">
                <ul>
                    <li><a href=""><i class="iconfont icon-shouji"></i><p>保障服务</p></a></li>
                    <li><a href=""></a></li>
                    <li><a href=""></a></li>
                    <li><a href=""></a></li>
                    <li><a href=""></a></li>
                    <li><a href=""></a></li>
                </ul>
            </div>
            <div class="home-promo-list">
                <ul>
                    <li><a href=""></a></li>
                    <li><a href=""></a></li>
                    <li><a href=""></a></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"home-hero"
}
</script>

<style lang="scss">
.home-hero{
    width: 1226px;
    margin: 0 auto;
}

.home-swiper{
    position: relative;
    ul li{
        position: absolute;
        height: 460px;
        width: 1226px;
        top: 0;
        left: 0;
    }
    .btn-rl{
        position: absolute;
        button{
            width: 40px;
            height: 70px;
            border-radius: 6px;
            background-color: rgb(255, 75, 105);
            position: absolute;
            top: calc(460px / 2 - 35px);
            i{
                font-size: 24px;
            }
        }
        .btn-left{
            left: 234px;
        }
        .btn-right{
            right: -1226px;
            transform: rotateZ(180deg);
        }
    }
    .btn-pagination{
        position: absolute;
        right: 26px;
        bottom: -436px;
        a{
            width: 6px;
            height: 6px;
            border-radius: 50%;
            border: 2px solid #999999;
            float: left;
            margin: 4px;
            background-color: #fff;
        }
    }
}

.home-list{
    width: 234px;
    height: 460px;
    background-color: rgba($color: #919191, $alpha: .3);
    position: relative;
    z-index: 10;

    ul{
        padding: 20px 0;

        li{
            height: 42px;
            a{
                display: block;
                height: 100%;
                width: 100%;
                line-height: 42px;
                position: relative;
                text-indent: 16px;
                color: white;

                &::after{
                    content: ">";
                    position: absolute;
                    right: 16px;
                    top: 0;
                    display: block;
                    height: 42px;
                    
                }
            }
        }
    }
}

.home-sub{
    margin: 14px 0 26px;
    height: 170px;
    .home-channel-list{
        float: left;
        height: 100%;
        width: 234px;
        margin-right: 14px;
        ul{
            display: flex;
            padding: 3px;
            align-content: space-between;
            justify-content: space-between;
            flex-wrap: wrap;
            li{
                width: 70px;
                height: 82px;
                padding: 0 3px;
                background-color: rgb(145, 95, 95);
                text-align: center;
                i{
                    font-size: 32px;
                    margin-top: 6px;
                    display: block;
                }
                p{
                    margin-top: -6px;
                }
            }
        }
    }
    .home-promo-list{
        float: left;
        height: 100%;
        width: calc(1226px - 248px);
        ul{
            display: flex;
            align-items: stretch;
            justify-content: space-between;
            li{
                width: 316px;
                height: 170px;
                background-color: rgb(216, 151, 151);
            }
        }
    }
}
</style>