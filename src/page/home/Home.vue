<template>
    <div class="home">
        <header>掌上书城</header>
        <div class="content">
            <!-- 轮播图组件 -->
           <CarouselFigure/>
           <div class="active-info">
               <span class="roll">
                <i class="fa fa-volume-up" aria-hidden="true"></i>
               <span>双11全场图书低至1折，更有隐藏神秘惊喜</span>
               </span>
           </div>
           <BookList/> 
        </div>
    </div>
</template>

<script>
import CarouselFigure from '@/components/CarouselFigure'
import BookList from '@/components/BookList'
export default {
    name: "Home",
    components:{
        CarouselFigure,
        BookList
    }
 
};
</script>

<style lang="scss" scoped>
    .active-info{
        height: 50px;
        line-height: 50px;
        font-size: 17px;
        font-weight: lighter;
        border-bottom: 1px solid #999;
        position: relative;
        &>.roll{
            display:inline-block;
            position: absolute;
            right:24px;
              overflow: hidden;
            animation:resizeRight 8s linear infinite;
           // animation:resizeLeft 5s linear 8s infinite;
        }
        & >.roll>i{
            display:inline-block;
            color: rgb(76, 224, 108);
        }
        & >.roll>span{
            display:inline-block;
          

        }
    }
    @keyframes resizeRight {
        from{right:-388px;}
        to{right:25px;}
    }
    
</style>