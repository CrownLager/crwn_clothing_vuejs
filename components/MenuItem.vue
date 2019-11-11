<template>
    <div :class="[size, 'menu-item']" @click="$router.push(linkUrl)">
        <div class='background-image' :style='{ backgroundImage: `url(${imageUrl}) `}' />
        <div class='content'>
            <h1 class='title'>{{title.toUpperCase()}}</h1>
            <span class='subtitle'>SHOP NOW</span>
        </div>
    </div>  
</template>

<script>
export default {
    name: "MenuItem",
    props: {
        title: String,
        imageUrl: String, 
        size: String,
        linkUrl: String
    }
}
</script>

<style lang="scss" scoped>
    .menu-item {
        min-width: 30%;
        height: 240px;
        flex: 1 1 auto;
        display: flex;
        align-items: center;
        justify-content: center;
        border: 1px solid black;
        margin: 0 7.5px 15px;
        overflow: hidden;

        &:hover {
            cursor: pointer;

            & .background-image {
                transform: scale(1.1);
                transition: transform 6s cubic-bezier(0.25, 0.45, 0.45, 0.95);
            }

            & .content {
                opacity: 0.9;
            }
        }


        &.large{
            height: 380px;
        }

        &:first-child {
        margin-right: 7.5px;
        }
    
        &:last-child {
        margin-left: 7.5px;
        }
        
        .background-image{
        width: 100%;
        height: 100%;
        background-position: center;
        background-size: cover;  
        }

        .content {
        height: 90px;
        padding: 0 25px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border: 1px solid black;
        background-color: white;
        opacity: 0.7;
        position: absolute;

        .title {
            font-weight: bold;
            margin-bottom: 6px;
            font-size: 22px;
            color: #4a4a4a;
        }
    
        .subtitle {
            font-weight: lighter;
            font-size: 16px;
        }
        }
    }
</style>