<template>
    <div id="array">
        <div class="element" v-for="height in heightArray">
            <div class="bar" v-bind:style="{ height: height}"></div>
        </div>
    </div>
</template>


<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class ElementArray extends Vue {
    
    private elements: Array<number> = [11, 3, 5, 1, 2, 7, 17, 8, 19, 16, 13, 14, 20, 12, 15, 4, 10, 18, 9, 6];

    // returns array containing relative (percentage) heights for each element
    get heightArray() {

        const max = Math.max(...this.elements);
        // construct height percentages
        return this.elements.map(v => 100 * (v / max) + "%");
    }
}
</script>

<style scoped lang="sass">

#array
    justify-self: flex-end
    height: 30%

    display: flex
    flex-flow: row nowrap
    justify-content: space-between
    
    .element
        flex-grow: 1
        padding-left: 3px
        padding-right: 3px
    
        display: flex
        justify-content: center
        align-items: flex-end
        
        .bar
            background-color: tomato
            width: 100%
</style>
