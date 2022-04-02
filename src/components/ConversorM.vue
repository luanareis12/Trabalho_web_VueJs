<template>
    <div class="conversor"><!--Onde vai conter todos os outros elementos-->
        <h2>{{moedaA}} Para {{moedaB}}</h2><!--mostrando  o título de um tipo de moeda para outro (ex: USD para BRL)-->
        <input type="text" v-model="moedaA_value" v-bind:placeholder="moedaA"><!--"v-bind:" foi usado para pegar o valor 
        da moedaA e "v-model" para pegar o valor que está dentro do input-->
        <input type="button" value="Converter" v-on:click="converter"> <!--"v-on:click" o botão para fazer a conversão-->
        <h2>{{moedaB_value}}</h2><!--Recebe o valor final da conversão-->
    </div>
</template>

<script>
export default { //vai receber os atributos do componente
    name: "ConversorM",
    props: ["moedaA", "moedaB"],//propriedades com os elementos em um array
    data(){//função para retornar um objeto que contém as propriedades 'moedaA_value e moedaB_value'.
        return{
            moedaA_value: "",//recebe vazio para mostrar o placeholder(o texto que aparece dentro do input)
            moedaB_value: 0 // inciar com zero
        };
    },
    methods:{//propriedade para declarar todos os métodos
        converter() {// para "ensinar" o programa como converter a moeda através do acesso de uma API
            let de_para= this.moedaA + "_" + this.moedaB;
            //fazendo acesso a uma API
            let url = 
            "https://free.currconv.com/api/v7/convert?q="+
            de_para +
            "&compact=ultra&apiKey=21f0e990344a7f49f0f3";
            fetch(url).then(res=> {// fecth(url) faz uma requisição para o endereço da API
                return res.json();
                //quando o fetch terminar vai executar o then com uma resposta que vai ser tranformada em um json
                }).then(json=>{
                    let cotacao = json[de_para];
                    this.moedaB_value = (cotacao * parseFloat(this.moedaA_value)).toFixed(2);//toFixed()-para deixar valores com 2 casas decimais no final
                    
                        2
                });
        },
    }
};
</script>
<!-- scoped- para definir um estilo apenas para o componente ConversorM -->
<style scoped> 
.conversor{
    padding: 20px;
    max-width: 300px;
    box-shadow: 0 4px 8px 0 rgba(40, 2, 252, 0.986);
    background-color: rgb(179, 179, 179);
}
</style>
<!--Obs: Sempre que é preciso passar por atributo algum valor que venha do script  é preciso 
utilizar algum dos elementos do  view que começa com o "v-", por exemplo "v-model="moedaA_value"
que está passando moedaA.-->