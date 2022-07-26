<!-- 검색 컴포넌트 -->
<template>
    <div id="searchBox">

        <!-- 검색 칸 -->
        <div class="input-group mb-3">
            <input type="text" class="form-control input-style" placeholder="지역, 지하철역 검색" aria-label="Recipient's username" aria-describedby="button-addon2">
            <button class="btn btn-outline-secondary btn-style" type="button" id="button-addon2">
                <i class="fa-solid fa-magnifying-glass"></i>
            </button>
        </div>

        <!-- 선택 조건 검색 -->
        <div class="container">
            <div class="row">

                <div class="col">
                    <div class="dropdown">
                        <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
                            전월세 지정
                        </button>
                        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                            <li><a class="dropdown-item" href="#">전체</a></li>
                            <li><a class="dropdown-item" href="#">전세</a></li>
                            <li><a class="dropdown-item" href="#">월세</a></li>
                            <li><hr/></li>
                            <!-- 보증금 지정 -->
                            <li>
                                <label for="customRange2" class="form-label" style="padding-left: 10px;">보증금&#160;&#58;&#160;{{deposit}}</label>
                                <input type="range" v-model="deposit" class="form-range dropdown-item" min="0" max="500000000" step="500000" id="customRange2">
                            </li>

                            <!-- 월세 지정 -->
                            <li>
                                <label for="customRange2" class="form-label" style="padding: 15px 0 0 10px;">월세&#160;&#58;&#160;{{monthly}}</label>
                                <input type="range" v-model="monthly" class="form-range dropdown-item" min="0" max="5000000" step="50000" id="customRange2">
                            </li>
                        </ul>
                    </div>
                </div>

                <!-- 방 구조 선택 -->
                <div class="col">
                    <div class="dropdown">
                        <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
                            방 구조 선택
                        </button>
                        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                            <li><a class="dropdown-item" href="#">전체</a></li>
                            <li><a class="dropdown-item" href="#">오픈형</a></li>
                            <li><a class="dropdown-item" href="#">분리형</a></li>
                            <li><a class="dropdown-item" href="#">복층형</a></li>
                        </ul>
                    </div>
                </div>

                <div class="col">
                    
                </div>
                
            </div>
        </div>

    </div>
</template>

<script>
export default {
    data() {
        return {
            deposit: 0, // 보증금
            monthly: 0, // 월세
        }
    },

    props: {

    }
}
</script>

<style scoped>
#searchBox{
    position: fixed;
    top: 110px;
    left: 30px;
    width: 360px;
    height: 100px;
    background: white;
    box-shadow: 0 5px 18px -7px rgba(0,0,0,1);
    border-radius: 5px;
}

i{
    color: white;
    font-size: 100;
}

.btn-style {
    border: 0.5px solid #EC9A39;
    box-sizing: border-box;
    background: #EC9A39;
}

.input-style {
    border: 0.5px solid #EC9A39;
    box-sizing: border-box;
    
}

</style>