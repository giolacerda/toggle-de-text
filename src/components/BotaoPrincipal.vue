<script>
export default {

    data() {
        return {
            textoBotao: false
        }
    },
     methods: {
        textoNaTela (){
            this.textoBotao = !this.textoBotao 
        }
     }

}
</script>


<template>
    <main class="corpo_botao">
     <button class="buttonPrincipal" @click="textoNaTela">Clique para ver o texto</button>
     <div v-if="textoBotao" class="textoVisivel">
        <p>Mensagem secreta desbloqueada 🔑</p>
     </div>
        
    </main>
</template>





<style scoped>
.corpo_botao {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.buttonPrincipal {

    background: linear-gradient(90deg, #4A90E2, #357ABD);
    color: white;
    font-weight: 600;
    padding: 0.6rem 1.2rem;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
    transition: background 0.3s ease, transform 0.2s ease;
}

.buttonPrincipal:hover {
    background: linear-gradient(90deg, #357ABD, #2C5F9E);
    transform: translateY(-2px);
}
</style>