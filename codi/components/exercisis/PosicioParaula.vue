<template>
    <v-container>
        <v-row>
            <v-col>
                <v-text-field v-model="valorActual">
                </v-text-field>
            </v-col>
            <v-col>
                <v-btn @click="mostraValor()">Posicio paraula</v-btn>
            </v-col>
            <v-col>
                <div>
                    {{resultat}}
                </div>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default{
        data(){
            return{
                valorActual:"",
                resultat:""
            }
        },
        methods:{
            mostraValor(){
                this.resultat=this.valorActual.split(" ").indexOf("hola")+1
            }
        }
    }
</script>