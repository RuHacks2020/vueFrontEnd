<template>
    <div id='nav'>
        <nav>
            <router-link v-for="routes in links"
            :key="routes.id"
            :to="routes.page">{{routes.text}}</router-link>
        </nav>       
    </div>
</template>
<script>
export default {
    name: 'Navigation',
    data(){
        return{
            links: [
                {
                    id:0,
                    text: 'KnockIO',
                    page:'/'
                    },
                    {
                    id:1,
                    text:'Home',
                    page:'/Home'
                    },
                    {
                    id:2,
                    text:'About',
                    page:'/About'
                    },
                ]
            }
        }
}
</script>
