<!-- 로그인 페이지 -->
<template>
    <div id="LoginPage">
        <div class="container">
            <div class="input-group mb-3">
                <span class="input-group-text" id="basic-addon1">ID</span>
                <input type="text" class="form-control" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
            </div>
            <div class="input-group mb-3">
                <span class="input-group-text" id="basic-addon1">PASSWORD</span>
                <input type="text" class="form-control" placeholder="Username" aria-label="Username" aria-describedby="basic-addon1">
            </div>
            <div class="input-group mb-3">
                <button type="button" class="btn btn-warning">로그인</button>
                
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "LoginPage",
    data() {
        return {

        }
    },

}
</script>

<style scoped>

</style>