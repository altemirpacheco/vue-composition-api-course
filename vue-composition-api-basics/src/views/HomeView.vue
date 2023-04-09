<template>
    <div class="home">
        <h1>Home</h1>
        <div>
            <button class="btn" @click="decreaseCounter">-</button>
            <span class="counter">{{ counter }}</span>
            <button class="btn" @click="increaseCounter">+</button>
        </div>
    </div>
</template>

<script setup>
import {ref} from "vue";

const counter = ref(0)
const increaseCounter = () => {
    counter.value++
}
const decreaseCounter = () => {
    counter.value--
}


</script>

<!--Composition API-->
<!--<script>-->
<!--    import {ref} from "vue";-->

<!--    export default {-->
<!--        setup(){-->
<!--            const counter = ref(0)-->
<!--            const increaseCounter = ()=> {-->
<!--                counter.value++-->
<!--            }-->
<!--            const decreaseCounter = ()=> {-->
<!--                counter.value&#45;&#45;-->
<!--            }-->

<!--            return{-->
<!--                counter,-->
<!--                increaseCounter,-->
<!--                decreaseCounter-->
<!--            }-->
<!--        }-->
<!--    }-->
<!--</script>-->

<!--Options API-->
<!--<script>-->
<!--export default {-->
<!--    data() {-->
<!--        return {-->
<!--            counter: 0-->
<!--        }-->
<!--    },-->
<!--    methods: {-->
<!--        increaseCounter() {-->
<!--            this.counter++-->
<!--        },-->
<!--        decreaseCounter() {-->
<!--            this.counter&#45;&#45;-->
<!--        }-->
<!--    }-->
<!--}-->
<!--</script>-->


<style scoped>
.home {
    text-align: center;
    padding: 20px;
}

.btn, .counter {
    font-size: 40px;
    margin: 10px;
}
</style>