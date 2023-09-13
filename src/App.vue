<!--
 * @Author: zhaoxf
 * @Date: 2023-08-04 15:22:51
 * @Description: 
-->
<template>
    <div id="app">
        <div id="nav">
            <Header></Header>
        </div>
        <router-view />
    </div>
</template>
<script>
import Header from './components/Header';
export default {
    components: {
        Header
    },
    data () {
        return {
            offsetY: 0, // 距离顶部高度
        }
    },
    mounted () {
        window.addEventListener('scroll', this.handleScroll)
    },
    methods: {
        toAbout () {
            this.$route.push({
                url: '/about'
            })
        },
        handleScroll () {
            console.log('滚动高度',window.pageYOffset);
            this.offsetY = window.pageYOffset;
            document.getElementById("nav").className = this.offsetY > 0 ? 'has-shadow' : '';
        }
    }
}
</script>

<style lang="scss">
html {
	height: 100%;
}
body {
	height: 100%;
	margin: 0;
}
#app {
	font-family: emoji;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    // text-align: center;
    color: #333333;
	height: 100%;
    width: 100%;
}

#nav {
    box-shadow: 0 0 20px #FFF;
    position: fixed;
    width: 100%;
    top: 0;
    background: #fff;
    transition: all ease .25s;
}
.has-shadow {
    box-shadow: 0 0 20px #00000008 !important;
}

::-webkit-scrollbar {
    /*滚动条整体样式*/
    width: 7px; /*高宽分别对应横竖滚动条的尺寸*/
    height: 7px;
}

::-webkit-scrollbar-thumb {
    /*滚动条里面小方块*/
    -webkit-box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
    background: #eaeaea;
    border-radius: 4px;
}

::-webkit-scrollbar-track {
    /*滚动条里面轨道*/
    -webkit-box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
    background: #fff;
}
</style>
