<script setup>
import Footer from "@/components/Footer.vue";
import Menu from "@/components/Menu.vue";
import MenuMobile from "@/components/MenuMobile.vue";

</script>

<template>

<div v-if="!isMobile()" class="marginMenu">
    <Menu
      :plotDropDown="true"
      :filter="filterDropdown"
      :actualCategory="$route.query.category"
    />
  </div>

  <div v-else>
    <MenuMobile
    :plotDropDown="true"></MenuMobile>
  </div>

    <div class="container">

        <div class="InfoLivro">

            <div imagem>
                <img src="..\assets\0.jpg" alt="capa do livro harry potter e a pedra filosofal">
            </div>

            <div style="margin-left:20px">  
                <div class="NomePreco">
                    <div class="Nome">
                        <div class="Titulo">
                            <span style="font-size:50px; weight:bold; color:black">Harry Potter e a Pedra Filosofal</span>
                        </div>

                        <div class="Autor">
                            <span style="font-size:20px; color:black">Rolling, J. K.</span>
                        </div>

                        <div class="Nota">
                            <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                            <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                            <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                            <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                            <img src="../components/icons/icons-estrela-vazia.png" class="imgAvaliacao" alt="estrela vazia">
                        </div>
                    </div>
                    <div class="Preco" style="display:flex; flex-direction: column; align-items: center;">
                        <div class="Valor">
                            <span style="color:black; weight:bold; font-size: 25px">R$ 39.90</span>
                        </div>

                        <div class="Botao">
                            <button type="button" class="btn btn-warning BotaoCarrinho " @click="goToCarrinho()" tabindex="15"> 
                                Adicionar ao carrinho
                                </button>

                            
                        </div>

                    </div>
                </div>

                <div class="Descricao" style="margin-top:30px">
                    <span style="color:black">Harry Potter ?? um garoto cujos pais, feiticeiros, foram assassinados por um poderos??ssimo bruxo quando ele ainda era um beb??. Ele foi levado, ent??o, para a casa dos tios que nada tinham a ver com o sobrenatural. Pelo contr??rio. At?? os 10 anos, Harry foi uma esp??cie de gata borralheira: maltratado pelos tios, herdava roupas velhas do primo gorducho, tinha ??culos remendados e era tratado como um estorvo. No dia de seu anivers??rio de 11 anos, entretanto, ele parece deslizar por um buraco sem fundo, como o de Alice no pa??s das maravilhas, que o conduz a um mundo m??gico. Descobre sua verdadeira hist??ria e seu destino: ser um aprendiz de feiticeiro at?? o dia em que ter?? que enfrentar a pior for??a do mal, o homem que assassinou seus pais. O menino de olhos verde, magricela e desengon??ado, t??o habituado ?? rejei????o, descobre, tamb??m, que ?? um her??i no universo dos magos. Potter fica sabendo que ?? a ??nica pessoa a ter sobrevivido a um ataque do tal bruxo do mal e essa ?? a causa da marca em forma de raio que ele carrega na testa. Ele n??o ?? um garoto qualquer, ele sequer ?? um feiticeiro qualquer; ele ?? Harry Potter, s??mbolo de poder, resist??ncia e um l??der natural entre os sobrenaturais. A f??bula, recheada de fantasmas, paredes que falam, caldeir??es, sapos, unic??rnios, drag??es e gigantes, n??o ??, entretanto, apenas um passatempo.</span>
                </div>
            </div>


        </div>

        <div class="DetalhesLivro">

            <div class="detalhes">
                <div class="Linha1">
                    <div class="Col1">
                        <span>Editora:</span>
                    </div>
                    <div class="Col2">
                        <span>Pottermore Publishing</span>
                    </div>
                </div>

                <div class="Linha2">
                    <div class="Col1">
                        <span>Autor:</span>
                    </div>
                    <div class="Col2">
                        <span>OLLY MOSS | J.K. ROWLING</span>
                    </div>
                </div>

                <div class="Linha1">
                    <div class="Col1">
                        <span>Tradutor:</span>
                    </div>
                    <div class="Col2">
                        <span>LIA WYLER</span>
                    </div>
                </div>

                <div class="Linha2">
                    <div class="Col1">
                        <span>Ano:</span>
                    </div>
                    <div class="Col2">
                        <span>1997</span>
                    </div>
                </div>

                <div class="Linha1">
                    <div class="Col1">
                        <span>P??ginas:</span>
                    </div>
                    <div class="Col2">
                        <span>352</span>
                    </div>
                </div>

                <div class="Linha2">
                    <div class="Col1">
                        <span>Edi????o:</span>
                    </div>
                    <div class="Col2">
                        <span>1</span>
                    </div>
                </div>

                <div class="Linha1">
                    <div class="Col1">
                        <span>Idioma:</span>
                    </div>
                    <div class="Col2">
                        <span>Portugu??s</span>
                    </div>
                </div>

                <div class="Linha2">
                    <div class="Col1">
                        <span>ISBN:</span>
                    </div>
                    <div class="Col2">
                        <span>9781408855652</span>
                    </div>
                </div>
            </div>

            <div class="avaliacoes">
                <div>
                    <span style="font-size:30px">Avalia????es</span>
                </div>
                <div  class="comentarios">
                    
                    <div class="Nota">
                        <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                        <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                        <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                        <img src="../components/icons/icons-estrela-vazia.png" class="imgAvaliacao" alt="estrela vazia">
                        <img src="../components/icons/icons-estrela-vazia.png" class="imgAvaliacao" alt="estrela vazia">
                    </div>
                    
                    <div>
                        <span style="font-size:20px; color: black;">Bom livro, mas p??ssima autora.</span>
                    </div>

                    <div class="Nota">
                        <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                        <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                        <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                        <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                        <img src="../components/icons/icons-estrela-cheia.png" class="imgAvaliacao" alt="estrela preenchida">
                    </div>
                    
                    <div>
                        <span style="font-size:20px; color: black;">Meu livro favorito quando era crian??a!</span>
                    </div>

                </div>
            </div>

        </div>

    </div>
    
    
    <Footer />
   
</template>

<script>
export default{
    methods:{isMobile() {
      if(window.screen.availWidth < 700){
        return true
        } else {
        return false
        }
        },
        goToCarrinho(){
      this.$router.push("/carrinho");

        }
    }
}
</script>
<style scoped>
.container{
    display: flex;
    margin-top: 150px;
    margin-bottom: 30px;
    flex-direction: column;
}
.InfoLivro{
    display: flex;
    border-style: solid;
    border-color:#e3dfd5;
    border-radius: 10px;
    padding: 40px;
    width: 100%;
    flex-wrap: wrap;
}

.NomePreco{
    display: flex;
    flex-direction: row;
    align-items: baseline;
    flex-wrap: wrap;
}

.Valor{
    background-color: rgb(232, 232, 232);
    height: 70px;
    width: 130px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.BotaoCarrinho{
    margin-top: 15px;
    height: 60px;
    width: 210px;
    background-color: #ffd117;
    color: rgb(0,0,3);
    font-weight:bold;
     font-family: "Open Sans", sans-serif;
  font-weight: bold;
}

.imgAvaliacao{
    width: 7%;
}

.DetalhesLivro{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top:30px;
    margin-bottom: 30px;
}
.detalhes{
    display: flex;
    flex-direction: column;
    width: 70%;
}

.Linha1{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    background-color: rgb(232, 232, 232);
    color:black;
    font-weight: bold;
}

.Linha2{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    background-color: rgb(195, 191, 191);
    color:black; 
    font-weight: bold;
}

.avaliacoes{
        margin-left: 60;
    }

@media (max-width: 768px) {
    .DetalhesLivro{
        flex-direction: column;
    }
    .avaliacoes{
        margin-left: 0;
    }
    .detalhes{
        width: 100%;
        margin-bottom: 10px;
    }
    .container{
        margin-top: 40px    ;
    }
}
</style>