<script>
export default {
    props:{
        RecentPost: Array
    }
}
</script>

<template lang="">
    <ul>
        <li v-for="(item,index) in RecentPost" :key="index"> <a href="`${item.url}`">{{ item.label }}</a>  </li>
    </ul>
</template>

<style lang="scss">
    .col-30{
        ul{
            list-style-type: none;
            a{
                color: white;
                text-decoration: none;
            }
            li{
                padding: 15px 0;
            }
        }
    }

    
</style>