<template>
    <div>
        <h2>{{msg}}</h2>
        <hr>
        <h3>{{$store.state.count}}</h3>
        <h2>{{count1}}</h2>
        <div>
            <!-- <button @click="$store.commit('add', 2)">+</button>
            <button @click="$store.commit('reduce')">-</button> -->

            <button @click="add(2)">+</button>
            <button @click="reduce">-</button>
        </div>
    </div>
</template>
<script>
//引入store文件
import store from "@/store/store";
import { mapState, mapMutations } from "vuex"; //用import引入mapState。
export default {
    props: {
        msg: String
    },

    computed: mapState({
        count1: 'count'
    }),
    methods: {
        ...mapMutations(['add', 'reduce']),
    },

    store
};
</script>