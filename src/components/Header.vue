<template>
    <header>
        <h3> {{message }} </h3>
        <NavList></NavList>

    </header>


</template>


<script>
    import NavList from './NavList.vue';

    export default {
    	props: ['message'],
        data () {
    		return {

            }
        },
        components: {
    		NavList
        }
    }
</script>

<style>

</style>