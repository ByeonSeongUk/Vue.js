<!-- 네비게이션 바 -->
<template>
    <div id="nav">
        <!-- 로고 버튼 -->
        <div id="logo">
            <a href="index.html">
                <img src="../assets/jigbangLogo.png" alt=""/>
            </a>
        </div>

        <!-- 메뉴 선택 -->
        <div>
            <ul id="navList">

                <!-- 메뉴 한칸 기준 -->
                <li>
                    <div class="dropdown">
                        <ul class="dropdown-toggle dropdown-remove-content" data-bs-toggle="dropdown" aria-expanded="false">
                            <li>원룸</li>
                            <li>전월세</li>        
                        </ul>
                
                        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                            <li><a class="dropdown-item dropdown-style" href="#">방 찾기</a></li>
                            <li><a class="dropdown-item dropdown-style" href="#">찜한 매물</a></li>
                            <li><a class="dropdown-item dropdown-style" href="#">방 내놓기&#40;전월세만&#41;</a></li>
                        </ul>
                    </div>
                </li>

            </ul>

            
        </div>


        <!-- 로그인 / 회원가입 버튼 -->
        <div class="form-group loginBtn">
            <button v-if="loginCheck == false" type="button" class="btn btn-secondary">
            <router-link to="/LoginPage">로그인 및 회원가입</router-link>
            </button>
            <button v-if="loginCheck == true" type="button" class="btn btn-secondary">회원명</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "navBar",

    data() {
        return {
            loginCheck: false
        }
    },


}
</script>

<style scoped>
#nav{
    width: 100%;
    height: 80px;
    margin-top: -20px;
    border-bottom: 0.5px solid RGB(225, 225, 225);
}


img {
    width: 120px;
    height: 70px;
    margin: 5px 0 0 10px;
}

ul, li {
    list-style: none;

}

#logo {
    float: left;
    width: 150px;
    height: 80px;
}

#navList > li {
    display: block;
    float: left;
    height: 50px;
    margin: 20px 20px 0 0;
    text-align: center;
}

#navList > li > div > ul > li:hover {
    cursor: pointer;
}

.loginBtn {
    float: right; 
    line-height: 80px; 
    margin-right: 50px;
}

/* 부트스트랩 수정 */
.dropdown-remove-content::after {
    content: none
}

.dropdown-remove-content > li:first-child {
    font-weight: bold;
    font-size: 18px
}

.dropdown-remove-content > li:last-child {
    font-weight: 400px;
    font-size: 12px
}

.dropdown-style {
    font-size: 12px;
    color: #333;
}
</style>