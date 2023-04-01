<template>
    <section v-if="show" class="calendarcard">
        <header>
            <small class="cardmonth">June 2022</small>

            <div></div>
        </header>
        <main >
            <ul class="main-days">
                <li><b>M</b></li>
                <li>T</li>
                <li>W</li>
                <li>T</li>
                <li>F</li>
                <li>S</li>
                <li>S</li>
            </ul>
            <ul class="main" >
                <li v-for="(item, index) in 30" :key={index} :class="{selectedDate: (selectedDate === item)}" @click="selectDate(item)">{{item }}</li>
            </ul>
        </main>
        <footer class="cardfooter">
            <div class="cardsecondarybutton">Cancel</div>

            <div class="cardprimarybutton">Done</div>
        </footer>
    </section>
</template>
<script setup>
import { reactive } from 'vue'
defineEmits(['selectDate'])
defineProps({
    show: Boolean
})

const state = reactive({ isSelected: false, selectedDate: 0 });


function selectDate(n) {
    state.isSelected = true;
    state.selectedDate = n;
        // emit('selectDate')
    }
</script>
<style scoped>
    .calendarcard {
        padding: 16px;
        background-color: var(--white);
        box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.1);
        border-radius: 8px; 
        margin-top: 16px;
    }
    .main, .main-days {
        display: grid;
        grid-template-columns: repeat(7, 1fr);
        column-gap: 30px;
        row-gap: 16px;
        list-style: none;
        text-align: center;
        padding-top: 16px;
        font-size: 12px;
        line-height: 14px;
    }

    .main-days {
        font-weight: 700;
    }

    .main:first-child {
        padding-top: 0px;
    }

    .cardfooter {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 12px;
        margin-top: 12px;
    }

    .cardprimarybutton {
        color: var(--white);
        background: #4B73DC;
        padding: 7px 34px;
        border-radius: 8px;
    }

    .cardsecondarybutton {
        background: var(--white);
        padding: 7px 34px;
        border-radius: 8px;
        border: 1px solid #4B73DC;
        color: #4B73DC;
    }

    .cardmonth {
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 700;
    }

    .selectedDate {
        background-color: red;
    }
</style>