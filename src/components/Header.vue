<template>
    <div class="header">
        <div class="header-text">
            <span class="accent">T</span>yamo
            <span class="accent">L</span>abo
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Homepage',
        head() {
            return {
                link: [
                   {
                        rel: 'stylesheet',
                        href:'https://fonts.googleapis.com/css?family=Vollkorn',
                    }
                ]
            }  
        }
    }
</script>

<style scoped lang="less">
@import "../variables.less";

.header-text {
    color: @black;
    font-size: 48px;
    font-weight: 100;
    font-family: 'Vollkorn', serif;
    .accent {
        color: @green;
    }
}
</style>
