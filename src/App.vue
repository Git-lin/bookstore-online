<template>
    <div id="app">
        <main>
            <router-view/>
        </main>
        <footer>
            <nav>
                <router-link tag="div" :to="{name: 'Home'}" exact>
                    <i class="fa fa-address-=+++ "></i>
                    <span>首页</span>
                </router-link>
                <router-link tag="div" :to="{name: 'Category'}">
                    <i class=""></i>
                    <span>分类</span>
                </router-link>
                <router-link tag="div" :to="{name: 'Cart'}">
                    <i class=""></i>
                    <span>购物车</span>
                </router-link>
                <router-link tag="div" :to="{name: 'Me'}">
                    <i class=""></i>
                    <span>我</span>
                </router-link>
            </nav>
        </footer>
    </div>
</template>

<script>
    import fontAwesome from 'font-awesome/css/font-awesome.css'
    export default {
        name: 'App'
    }
</script>

<style lang="scss">
    $theme-color: #35a5eb;
    *,*::before,*::after {
        box-sizing: border-box;
    }
    html,body {
        height: 100%;
        font: 24px "Microsoft YaHei",sans-serif,Arial;
    }
    #app {
        height: 100%;
        & > main {
            $header-height: 40px;
            height: calc(100% - 44px);
            & > div {
                height: 100%;
                padding-top: $header-height;
                & > header {
                    width: 100%;
                    height: 40px;
                    line-height: 40px;
                    background-color: $theme-color;
                    text-align: center;
                    color: #ffffff;
                    position: absolute;
                    left: 0; top: 0;
                }
                .content {
                    height: 100%;
                    overflow-x: hidden;
                    overflow-y: auto;
                }
            }
        }
        & > footer {
            height: 44px;
            line-height: 44px;
            color: white;
            background-color: $theme-color;
            nav {
                display: flex;
                justify-content: space-around;
                div {
                   // padding: 6px;
                }
            }
        }
    }

</style>
