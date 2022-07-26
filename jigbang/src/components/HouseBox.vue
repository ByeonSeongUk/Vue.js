<!-- 매물 리스트 -->
<template>
    <div id="HouseBox">
        <div id="houseBoxInfo">
            <div class="hb_list">
                <span>지역 목록 OO 개</span>
            </div>
            <div class="hb_unit">
                <a href="#">단위</a>
            </div>
        </div>
        <HouseList/>
        <HouseList/>
        <HouseList/>
        <HouseList/>
        <HouseList/>
        <HouseList/>
        <HouseList/>
        <HouseList/>
        <HouseList/>
        <HouseList/>
        <HouseList/>
    </div>
</template>

<script>
import HouseList from './HouseList.vue';

export default {
    name: 'HouseBox',
    
    components: {
        HouseList
    }

}
</script>

<style scoped>
#HouseBox {
    float: right;
    width: 400px;
    height: calc(100vh - 80px);;
    overflow-y: scroll;
}

#houseBoxInfo {
    display: flex;
    width: 100%;
    height: 50px;
    border: 1px solid rgb(225, 225, 225);
    background: white;
}

.hb_list {
    width: 80%;
    height: 100%;
    line-height: 50px;
    background: violet;
}

.hb_list > span {
    font-weight: 600;
    margin-left: 10px;
}

.hb_unit {
    width: 20%;
    height: 100%;
    line-height: 50px;
    text-align: center;
    background: turquoise;
}

</style>