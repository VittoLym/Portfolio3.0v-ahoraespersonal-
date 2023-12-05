<script setup>
const props = defineProps(['showNav'])
const tagsHeader = ['Home','Projects','Skills','About Me']
</script>
<template>
    <header>
        <Transition name="visibility">
            <ul v-if="showNav"  key="component" class="comp-animated">
                <li v-for="tag in tagsHeader" :key="tag">
                <a :href="'#'+tag" >{{ tag }}</a>
                </li>
            </ul>
        </Transition>
    </header>
</template>
<style scoped>
header {
    height: 36vh;
    position: fixed;
    top: 32vh;
    display: flex;
    flex-direction: column;
    left: .5vw;
}
ul{
    padding: 0;
}

ul li a {
    color: #9370db;
    text-decoration: none;
    transition: all ease .5s;
    font-size: 1.5rem;
    font-weight: bold;
}

ul li a:hover {
    color: #6532cc;
    border-bottom: solid 5px #9370db;
}

ul li {
    transition: transform .5s ease;
    list-style: none;
    margin: 2vh 0;
    text-align: start;
}
ul li:hover{
    transform: translateX(20px);
}
.visibility-enter-active {
    transition: all 1s ease;
}
.visibility-leave-active {
    transition: all .5s ease;
}
.visibility-enter-from, .visibility-leave-to{
    opacity: 0;
    transform: translateX(-40px);
}
</style>