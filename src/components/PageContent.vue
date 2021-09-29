<template>
    <section class="PageContent">     
        <div class="container page-content">
            <p>-->Content goes here&lt;--</p>
        </div>
    </section>
</template>

<script>
export default {
    name: "PageContent"
}
</script>

<style scoped lang="scss">
    @import '@/assets/style/common';
    @import '@/assets/style/variables';

    .PageContent {
        background-color: $grey100;
        padding: $sectionPadding;
        font-size: 1.375rem;
        font-weight: 700;
    }
</style>