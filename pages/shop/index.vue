<template>
    <div class='shop-page'>
        <CollectionPreview v-for="collection in collections" :key="collection.id" v-bind="collection" />

    </div>            
</template>

<script>
import CollectionPreview from '../../components/CollectionPreview.vue';

import SHOP_DATA from './shop.data.js';

export default {
    components: {
        CollectionPreview
    },
    computed: {
        collections: () => {
            return SHOP_DATA;
        }
    }
}
</script>

<style>

</style>