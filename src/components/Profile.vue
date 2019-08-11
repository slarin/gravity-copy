<template>
    <div class="p-div">
        <img :src="src"/>
        <div>
            <p class="bg-txt">{{name}}</p>
            <p class="sm-txt">{{position}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Profile',
    
    props: {
        src: null,
        name: String,
        position: String
    }
}
</script>

<style>
    .p-div{
        display:flex;
        flex-flow: row nowrap;
        justify-content: space-evenly;
        margin-top: 30px;
    }
    .p-div > img{
        object-fit: contain;
        margin: 0px -20px 0px 0px;
    }
    .p-div > div{
        display: flex;
        margin-left: 35px;
        flex-flow: column nowrap;
        align-items: flex-start;
        line-height: 0;
    }
    .bg-txt{
        font-size: 15px;
        font-weight: bold;
    }
    .sm-txt{
        font-size: 10px;
        font-weight: lighter;
        margin-top: 2px;
        text-align: left;
    }

</style>