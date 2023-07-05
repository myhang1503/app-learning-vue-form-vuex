<template>
  <section class="container">
    <h1>Demo Form</h1>
    <form @submit.prevent="handleSubmit">
        <div class="form-group">
            <label for="taiKhoan">Tai Khoan</label>
            <input type="text" class="form-control" id="taiKhoan" v-model.trim="taiKhoan"/>
        </div>
        <div class="form-group">
            <label for="baiLam">Bai lam</label>
            <textarea class="form-control" id="baiLam" rows="5" v-model="vanMau"></textarea>
        </div>
        <div class="form-group form-check">
            <input type="checkbox" class="form-check-input" id="isSave" v-model="isSave">
            <label class="form-check-label" for="isSave">Luu mat khau</label>
        </div>

        <div>
            <h3>Ban muon song o dau?</h3>
        </div>
        <div class="form-group form-check">
            <input type="checkbox" class="form-check-input" value="HCM" v-model="places">
            <label class="form-check-label">HCM</label>
        </div>
        <div class="form-group form-check">
            <input type="checkbox" class="form-check-input" value="DaLat" v-model="places">
            <label class="form-check-label">DaLat</label>
        </div>
        <div class="form-group form-check">
            <input type="checkbox" class="form-check-input" value="Hue" v-model="places">
            <label class="form-check-label">Hue</label>
        </div>

        <div>
            <h3>Loai nguoi dan</h3>
            <div class="form-check">
                <input class="form-check-input" type="radio" value="binhThuong" v-model="status">
                <label class="form-check-label"> Binh Thuong </label>
            </div>
            <div class="form-check">
                <input class="form-check-input" type="radio" value="ngheo" v-model="status">
                <label class="form-check-label"> Ngheo </label>
            </div>
            <div class="form-check">
                <input class="form-check-input" type="radio" value="canNgheo" v-model="status">
                <label class="form-check-label"> Can ngheo </label>
            </div>
        </div>

        <div>
            <label class="my-1 mr-2">Chon lop hoc</label>
            <select class="custom-select my-1 mr-sm-2" v-model="lop">
                <option value="1">One</option>
                <option value="2">Two</option>
                <option value="3">Three</option>
            </select>
        </div>

        <div class="form-group">
            <label>Age</label>
            <input type="number" class="form-control" v-model="age"/>
            <input type="text" class="form-control" v-model.number="agenum"/>
        </div>

        <button class="btn btn-success" type="submit">Submit</button>
    </form>
  </section>
</template>

<script>
export default {
    data(){
        return{
            taiKhoan: "",
            vanMau: "testing",
            isSave: false,
            places: [],
            status: "",
            lop: 1,
            age: 0,
            agenum: 0,
        };
    },
    methods:{
        handleSubmit(){
            console.log(this.taiKhoan);
            console.log(typeof this.agenum);
        }
    }
}
</script>

<style>

</style>