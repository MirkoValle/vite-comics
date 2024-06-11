<script>
export default{
    data() {
        return{
            
        }
    },
    props:{
        singleComic:{
            type: Object,
            required: true,
        }
    }
}
</script>

<template>
<article>
    <img :src="singleComic.thumb" :alt="singleComic.series">
    <h4>
        {{ singleComic.series }}
    </h4>
</article>
</template>

<style lang="scss" scoped>

    article{
        width: calc((100% / 6) - 2rem);
        padding: 1rem;

        img{
            width: 100%;
            aspect-ratio: 1/1;
            object-fit: cover;
            object-position: top;
        }
        h4{
            color: white;
        }
    }

</style>