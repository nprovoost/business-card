<template>
    <div class="body__profile__photo">
    <img src="https://scontent-bru2-1.xx.fbcdn.net/v/t1.6435-1/49948921_10216823807562005_1048180450691907584_n.jpg?stp=dst-jpg_s200x200&_nc_cat=107&ccb=1-7&_nc_sid=7206a8&_nc_ohc=7Qd-iPUOTcwAX86nQpQ&_nc_ht=scontent-bru2-1.xx&cb_e2o_trans=q&oh=00_AfC3-FN_5g_MkBXOmRNDjJh3qE3ZdLF_BEJAhUnqIOuUpg&oe=6543B695" alt="Perfil" />   
    </div>
</template>

<script>
export default {
    name: "Photo"
}
</script>

<style>
    .body__profile__photo img {
        border-radius: 50%;
        width: 200px;
        height: 200px;
        border: 15px solid #fff;
        top: -100px;
        position: relative;
        box-shadow: 1px 2px 18px 4px rgb(226, 226, 226);
    }
</style>

