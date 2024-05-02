<template>
    <form @submit="handleSubmit" @mouseenter="updateTheme">
        <p>{{ movie?.name }}</p>
        <button type="submit" @click="decrementCount" :disabled="count <= 0">-</button>
        {{ count }}
        <button type="submit" @click="incrementCount" :disabled="count >= movie?.maxTickets">+</button>
        <div class="divButton">
            <nuxt-link :to="{ name: 'pay', query: { name: movie?.name, count } }">
                <p class="pagarButton">Pagar</p>
            </nuxt-link>
        </div>
    </form>
</template>
  
<script>
    export default {
        data() {
            return {
                count: 0
            };
        },
        props: {
            movie: Object
        },
        methods: {
            handleSubmit(event) {
                event.preventDefault();
            },
            decrementCount() {
                this.count--;
            },
            incrementCount() {
                this.count++;
            },
            updateTheme() {

            }
        }
    };
</script>
  
<style scoped>
    form {
        text-align: center;
        color: white;
    }
    
    button {
        --border-color: #000; /* Define CSS variable */
        
        cursor: pointer;
        padding: 6px 6px;
        margin: auto 1.2vw;
        border: 1px solid var(--border-color); /* Use CSS variable */
        border-radius: 9px;
        transition: 150ms border-color;
    }
    
    button:hover {
        --border-color: #4781FF; /* Change CSS variable value on hover */
    }
    
    button[disabled] {
        background: #4781FF;
    }
    
    .divButton {
        transform: translateY(0.9vh);
        display: flex;
        justify-content: center;
    }
    
    .pagarButton {
        color: white;
        text-align: center;
        background-color: #4781FF;
        width: 30vh;
        border-radius: 12px;
        padding: 6px 0 6px;
    }
    
    .pagarButton:hover {
        color: yellow;
        transform: scale(1.2);
    }
</style>
