<!--
 * @Author: zhaoxf
 * @Date: 2023-08-29 11:34:19
 * @Description: Header
-->
<!--
* www.cloudscope.cn
* Copyright (c) 2019. All Rights Reserved.
-->
<template>
    <div class="header-container">
        <div class="logo">
            <img src="../assets/images/logo.png" alt="">
        </div>
        <div class="menus">
            <span>Features</span>
            <span>Contact</span>
            <span>Subscribe</span>
        </div>
    </div>
</template>

<script>
export default {
    data () {
        return {
        };
    },

    components: {},

    computed: {},

    mounted () {},

    methods: {}
};

</script>
<style lang='scss' scoped>
.header-container {
    width: 50%;
    padding: 10px 40px;
    min-width: 700px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    height: 40px;
    line-height: 40px;
    font-size: 16px;
    color: #666;
}
.logo {
    img {
        height: 40px;
        border-radius: 50%;
    }
}
.menus {
    span {
        display: inline-block;
        margin-left: 30px;
        transition: all ease .25s;
        cursor: pointer;
        position: relative;
        &:first-child {
            margin: 0;
        }
        &::after {
            content: '';
            display: inline-block;
            width: 0;
            height: 2px;
            background: #fff;
            position: absolute;
            bottom: 0;
            left: 50%;
            transition: all ease .25s;
        }
        &:hover {
            color: #999;
            &::after {
                content: '';
                width: 100%;
                left: 0;
                background: #999;
            }
        }
    }
}
</style>