# NLW_IA
Trilha Foundation - Shorts Summary

Shorts Summary é uma aplicação web para criar resumo de vídeos shorts do Youtube utilizando Inteligência Artificial para transcrever o conteúdo do vídeo e realizar o resumo do conteúdo Esse projeto é desenvolvido na trilha Foundations na edição NLW AI.

-> Criar o conteúdo do vídeo em texto 

-> Criar um resumo apartir do texto

- [x] Frontend
- [x] Vite Install
- [x] express
- [x] cors
- [x] axios
- [x] ytdl-core 4.10.0 (biblioteca que permite baixar vídeos do youtube)

<!--
A pasta que começa com . é uma pasta oculta


no arquivo packge.json
"ytbdl-core": "^4.10.0"

o ^ indica que sempre que vai rodar o comando npm vai buscar a ultima versão. se você que manter a versão fixa você retira o acento.


    // "server": "env YTDL_NO_UPDATE=1 node --watch --no-warnings server/index.js"
remover alertas



Por padrão os eventos de submit recarregam a página imediatamente 
se você quer que isso não aconteça: você deve recuperar o evento e usar preventDefault()

form.addEventListener("submit",(event)=>{
    event.preventDefault()
    console.log("Dados Enviados!")
})
-->