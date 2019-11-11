<template>
    <div class='collection-preview'>
        <h1 class='title'>{{title.toUpperCase()}}</h1>
        <div class="preview">
            <CollectionItem v-for="item in items.filter((_,idx) => idx < 4)" :key="item.id" v-bind="item" />
        </div>
        </div>
    </div>
</template>

<script>
import CollectionItem from './CollectionItem.vue';

export default {
    components: {
        CollectionItem
    },
    props: {
        title: String,
        items: Array
    }

}
</script>

<style lang="scss" scoped>
    .collection-preview {
        display: flex;
        flex-direction: column;
        margin-bottom: 30px;
    
        .title {
        font-size: 28px;
        margin-bottom: 25px;
        }
    
        .preview {
        display: flex;
        justify-content: space-between;
        }
    }  
</style>