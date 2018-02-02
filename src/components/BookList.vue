<template>
    <div class="book-list">
        <h2>
            新书上架
        </h2>
        <ul>
            <li>
                <img src="../assets/img/3.jpg">
                <div class="book-name">java高级程序设计</div>
                <div class="book-price">￥65.30</div>
            </li>
            <li>
                <img src="../assets/img/3.jpg">
                <div class="book-name">java高级程序设计</div>
                <div class="book-price">￥65.30</div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'BookList',
        data() {
            return {

            }
        }
    }
</script>

<style lang="scss" scoped>
.book-list{
    padding: 10px;
    & >h2{
        font-size: 18px;
    }
    & >ul{
        list-style:none;
        display: flex;
        justify-content: space-between;
    }
}
</style>