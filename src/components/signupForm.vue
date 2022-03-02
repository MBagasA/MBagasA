<template>

<form @submit="handleSubmit">
<p>Contact Management</p>
    <label>Email:</label>
    <input type="email" required v-model="email">

    <label>Nama Lengkap:</label>
    <input type="namalengkap" required v-model="namalengkap">

    <label>Alamat:</label>
    <input type="alamat" required v-model="alamat">

    <label>No Hp:</label>
    <input type="nohp" required v-model="nohp">

    <label>Posisi : </label>
    <select v-model="posisi">
        <option value = "developer"> web developer</option>
        <option value = "designer">web design</option>
    </select>
    <div class="setuju">
    <input type="checkbox" required>
    <label>setuju</label>
    </div>

    <div class="submit">
    <button>kirim</button>
    </div>
</form>
</template>

<script>
export default{
    data(){
        return{
            email: '',
            namalengkap: '',
            alamat: '',
            nohp: '',   
            posisi: '',
            setuju:false
        }
        
    }
}
</script>

<style>
    form{
        max-width:420px;
        margin:30px auto;
        background:white;
        text-align:left;
        padding:40px;
        border-radius:10px;
        font: sans-serif;
    }
    label{
        color: #333;
        display: inline-block;
        margin: 25px 0 15px;
        font-size: 0.8rem;
        text-tranform:uppercase;
        letter-spacing:1px;
        font-weight:bold;

    }

    input, select{
        display:block;
        padding:10px 6px;
        width:100%;
        box-sizing:border-box;
        border:none;
        border-bottom:1px solid #ddd;
        color: #555;
    }

    input[type="checkbox"]{
        display: inline-block;
        width:16px;
        margin: 0 10px 0 0;
        position: relative;
        top:2px
    }
    button{
        background:#0b6dff;
        border:0;
        padding:10px 20px;
        margin-top:20px;
        color:white;
        border-radius: 20px;
    }
    .submit{
        text-align:center;
    }
</style>