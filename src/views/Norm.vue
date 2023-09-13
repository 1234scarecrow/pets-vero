<!--
 * @Author: zhaoxf
 * @Date: 2023-08-28 16:21:52
 * @Description: 
-->
<!--
* www.cloudscope.cn
* Copyright (c) 2019. All Rights Reserved.
-->
<template>
    <div class="content">
        <div class="font-color">
            <p class="title">1. 字体颜色</p>
            <span class="el-icon-info primary-color"></span>
            <span class="el-icon-info secondary-color"></span>
            <span class="el-icon-info tip-color"></span>
            <span class="el-icon-info theme-color"></span>
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
.content {
    padding: 20px;
    font-size: 18px;
    > {
        div {
            border-bottom: 1px solid #000;
            padding: 20px 0;
        }
    }
}
.title {
    font-size: 18px;
    color: #333;
}
.font-color {
    span {
        display: inline-block;
        width: 20px;
        height: 20px;
        border-radius: 10px;
        margin: 0 10px;
        font-size: 20px;
        font-weight: bold;
    }
}
</style>