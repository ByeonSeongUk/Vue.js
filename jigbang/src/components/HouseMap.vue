<!-- 지도 -->
<template>
    <div id="map">
        <SearchBox></SearchBox>
        <HouseBox></HouseBox>
    </div>
</template>

<script>

import SearchBox from './SearchBox.vue'
import HouseBox from './HouseBox.vue'


export default {
    name: 'app',

    components: {
        SearchBox,
        HouseBox,
    
    }
}
</script>

<style scoped>
#map {
    width: 100%;
    height: calc(100vh - 80px);
    background:cornsilk;
}
</style>