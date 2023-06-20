<template>
    <v-container>
        <v-row no-gutters>
            <v-col cols="12"> 
                <v-card
                    :loading="false"
                    title="Teste de API"
                    variant="tonal"
                    subtitle="Teste para verificar se a comunicação entre o cliente e API está correta"
                >
                    <v-card-text>
                        <v-col cols="12" class="mx-0 px-0" v-if="consultaExecutada">
                            <div class="font-weight-bold mx-0 px-0">
                                Resultado:
                            </div>
                        </v-col>
                    </v-card-text>
                    <v-card-actions>
                        <v-btn color="green-darken-1" variant="tonal" @click="consultar()">Executar</v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script lang='ts'>
import { defineComponent } from 'vue';
import HelloWorld from '@/components/HelloWorld.vue'
import axios from 'axios'

interface Todo {
  text: string;
}

const App = defineComponent({
  components: {
    HelloWorld
  },

  data() {
    return {
      response: false,
      consultaExecutada: false,
      serverUrl: import.meta.env.VITE_SERVER_URL
    };
  },
  methods: {
    consultar(){
        alert(this.serverUrl)
    }
  },

  mounted(){
  }
});

export default App
</script>
