<template>
    <MainLayout page-title="Checkout">
        <section class="imagecontainer">
            <div>
                <img src="~/assets/img/nuxt.png" alt="Discover Nuxt 3" />
            </div>
            <div>
                <h4 class="pb">Biking</h4>
                <small class="pricing-items">London,Ontario</small>

                <div class="users"> 
                    <div class="circleimgcontainer">
                        <img class="circleimg" src="~/assets/img/nuxt.png" alt="Discover Nuxt 3" />
                        <img class="circleimg" src="~/assets/img/nuxt.png" alt="Discover Nuxt 3" />
                        <img class="circleimg" src="~/assets/img/nuxt.png" alt="Discover Nuxt 3" />
                        <img class="circleimg" src="~/assets/img/nuxt.png" alt="Discover Nuxt 3" />
                    </div>

                    <p>+30</p>
                </div>
                
            </div>
        </section>
        <h4 class="pb">Your Activity Details</h4>
        <div class="semiheader">
            <h5>Date</h5>

            <NuxtLink to="#">Edit</NuxtLink>
        </div>
        <p class="pb">June 22,30th</p>
        <div class="semiheader">
            <h5>Guest</h5>

            <NuxtLink to="#">Edit</NuxtLink>
        </div>
        <p class="pbtwo">2 Adults, 0 Children</p>
        <div class="pricing-items">
            <p>$38.50x 2 adult guests</p>

            <p>$77</p>
        </div>
        <div class="pricing-items">
            <p>$4.50 taxes</p>

            <p>$4.50</p>
        </div>
        <div class="total">
            <p>Total(CAD)</p>

            <p>$81.50</p>
        </div>
        <h4 class="pb">Pricing</h4>
        <div class="space-between">
            <h4>Pay With</h4>

            <NuxtLink to="#">Edit</NuxtLink>
        </div>

        <div class="creditcardcontainer">
            <div class="space-between">
                <p>Jason Malta</p>
                <p>07/25</p>
            </div>
            <div class="space-between"> 
                <p>.........</p>

                <p>VISA</p>
            </div>
        </div>
        <Buttonbottom>
            <Button label="Make a Payment" :isDisabled={isButtonDisabled} @click={makePayment} />
        </Buttonbottom>
    </MainLayout>
</template>
<script setup>
import MainLayout from '~/Layout/Mainlayout.vue';
import Buttonbottom from '~/components/Buttonbottom.vue';
import Button from '~/components/Button.vue'
import { reactive } from 'vue';

let state = reactive({
    isButtonDisabled: true
})

function makePayment() {
    console.log(state.isButtonDisabled)
    state.isButtonDisabled = false
}

</script>

<style scoped>
    .space-between, .semiheader, .pricing-items, .total{
        width: 100%;
        height: auto;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }

    .semiheader {
        margin-bottom: 5px;
    }

    .pb {
        padding: 0px 0px 8px 0px;
    }

    .pbtwo {
        margin-bottom: 17px;
    }

    .pricing-items {
        margin-bottom: 11.54px;
    }

    .total {
        margin-bottom: 22.67px;
    }

    .creditcardcontainer {
        width: 100%;
        background: #1F2D4F;
        box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.1);
        border-radius: 8px;
        padding: 16px 12px;
        margin-top: 10px;
        display: flex;
        flex-direction: column;
        gap: 7px;
        color: var(--white)
    }

    .imagecontainer {
        display: grid;
        grid-template-columns: 221px auto;
        gap: 16px;
        margin-bottom: 20px;
    }

    .circleimg {
        height: 24px;
        width: 24px;
        border-radius: 50%;
    }

    .circleimg:nth-child(1) {
        z-index: 4;
    }

    .circleimg:nth-child(2) {
        z-index: 3;
        position: absolute;
        left: 12px;
    }

    .circleimg:nth-child(3) {
        z-index: 2;
        position: absolute;
        left: 24px;
    }

    .circleimg:nth-child(4) {
        position: absolute;
        right: 0;
        top: 0;
        z-index: 1;
    }

    .circleimgcontainer {
        position: relative;
        display: flex;
        flex-direction: row;
        width: 60px;
        height: 24px;
    }

    .users {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 8px;
    }
</style>