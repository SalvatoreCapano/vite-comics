<script>

export default {
    name: 'SeriesCard',
    props: {
        title: String,
        url: String
    },
}
</script>


<template>

    <div>
        <div class="imgContainer">
            <img :src="url" alt="title">
        </div>

        <h3 class="seriesTitle">{{ title }}</h3>
    </div>

</template>


<style lang="scss" scoped>
    @import "../styles/partials/mixin.scss";

    .imgContainer {
        width: 100%;
        height: 165px;

        margin-bottom: 0.75rem;
        img {
            width: 100%;
             height: 100%;
            object-fit: cover;
            object-position: top;
        }
    }

    .seriesTitle {
        color: #ffffff;
        text-transform: uppercase;
        font-size: 1rem;
                    
    }

</style>