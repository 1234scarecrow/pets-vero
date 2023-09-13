<!--
 * @Author: zhaoxf
 * @Date: 2023-08-04 15:22:51
 * @Description: 
-->
<template>
    <!--  @mousewheel.prevent="changePage" -->
    <div class="home" ref="home" id="Home" >
        <div class="page content">
            <div class="text-container">
                <!-- <img class="logo" src="../assets/images/pet.png" alt=""> -->
                <p class="word">A miniprogram</p>
                <p class="word">For Pet Lovers</p>
                <p class="word">No need to worry about losing the vaccine</p>
                <p class="word large">AND ...</p>
                <p class="word">Visual health</p>
                <p class="word">Immediate reminder</p>
            </div>
            <div class="img-container">
                <img class="demo" src="../assets/images/minipro-demo1.png" alt="">
            </div>
        </div>
        <!-- <div class="page target" ref="target" style="background: #e6eff9;">
            <span class="text">Hello Pets~{{pageNo}}</span>
        </div>
        <div class="page" style="background: #ffe8e6;">
            <span class="text">Page2{{pageNo}}</span>
        </div>
        <div class="page" style="background: #ffddef;">
            <span class="text">Page3{{pageNo}}</span>
        </div>
        <div class="page" style="background: #dfffeb;">
            <span class="text">Page4{{pageNo}}</span>
        </div> -->
    </div>
</template>

<script>
export default {
    name: 'Home',
    components: {},
	computed: {},
    methods: {
        changePage (e) {
            let pages = document.getElementsByClassName('page');
			const stageHeight = pages[0].clientHeight;
			console.log(stageHeight);
            if (e.wheelDelta === -120) {
				if (- this.$refs.target.style.marginTop.match(/\d+/g) - stageHeight >= - stageHeight * 3) {
                	this.$refs.target.style.marginTop = - this.$refs.target.style.marginTop.match(/\d+/g) - stageHeight + 'px'
				}
            } else {
				if (- this.$refs.target.style.marginTop.match(/\d+/g) + stageHeight <= 0) {
					this.$refs.target.style.marginTop = - this.$refs.target.style.marginTop.match(/\d+/g) + stageHeight + 'px'
				}
			}
        }
    },
}
</script>
<style scoped lang="scss">
.home {
    height: calc(100% - 81px);
    overflow: hidden;
    .text {
        font-family: fantasy;
        font-size: 30px;
    }
}
.page {
    height: 100%;
    position: relative;
    background: #953bec;
    .text {
        display: inline-block;
        width: 100%;
        height: 50px;
        line-height: 50px;
        text-align: center;
        position: absolute;
        top: calc(50% - 25px);
        transform: translateX(-50%);
    }
}
.content {
    position: relative;
    .demo {
        width: 50%;
        // transform: scale3d();
        margin-left: 500px;
    }
}
.text-container {
    position: absolute;
    top: 50px;
    left: 150px;
}
.text-container .word {
    color: white;
    font-size: 28px;
    text-align: left;
    text-shadow:  5px 5px 10px #26095b;
}
.large {
    font-size: 34px;
}
.img-container {
    background: linear-gradient(#7030e6, #7030e7 71%, #953bec 97%);
}
.target {
	transition: all ease .75s;
}
// l5CKgZO8wjg%H@2g
// Eeht_3xne-UbWGxNrkZLkQZK-A5z
</style>
