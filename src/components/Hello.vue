<template>
    <div>
        <div class="greeting">{{ msg }} {{ exclamationMarks }}</div>
        <button @click="decrement">-</button>
        <button @click="increment">+</button>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Prop } from "vue-property-decorator";
import Component from 'vue-class-component';

@Component({
    name: 'HelloComponent',
})
export default class Hello extends Vue {
    @Prop()
    msg: string

    @Prop()
    initialEnthusiasm: number

    enthusiasm = this.initialEnthusiasm

    increment(): void {
        this.enthusiasm++;
    }

    decrement(): void {
        if (this.enthusiasm > 1) {
            this.enthusiasm--;
        }
    }

    get exclamationMarks(): string {
        return Array(this.enthusiasm + 1).join('!');
    }
}
</script>

<style>
    .greeting {
        font-size: 20px;
    }
</style>