# Shorts Summary NLW_IA
Trilha Foundation - Shorts Summary

Shorts Summary é uma aplicação web para criar resumo de vídeos shorts do Youtube utilizando Inteligência Artificial para transcrever o conteúdo do vídeo e realizar o resumo do conteúdo Esse projeto é desenvolvido na trilha Foundations na edição NLW AI.

-> Criar o conteúdo do vídeo em texto 

-> Criar um resumo apartir do texto

No projeto será usado dois modelos da OPENAI: Whisper (modelo da OpenAi de reconhecimento automático de fala (ASR - automatic speech recognition)) e o modelo Bart (Modelo para resumo de texto)

transformer.js : Permite utilizar modelos de IA no navegador e servidor com Javascript. E Fornece modelos pré-treinados para realizar diversas tarefas. Modelos: https://huggingface.co/models

- [x] Frontend
- [x] Vite Install
- [x] express
- [x] cors
- [x] axios
- [x] ytdl-core 4.10.0 (biblioteca que permite baixar vídeos do youtube)

- [x]


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



npm i @xenova/transformers fluent-ffmpeg ffmpeg-static node-wav

Você vai no site hugging face e vai buscar um modelo em uma categoria (resumo, processamento de liguagem natural,...) da xenova

- Exemplo de resumo
A estrutura do código:

import { pipeline } from "@xenova/transformers"

const generator = await pipeline(
    "summarization",
    "Xenova/distibart-cnm-12-6"
)

const output = await generator(text)
return output[0].summary_text


- Exemplo da transcrição de audio para texto

import { pipeline } from "@xenova/transformers"

const transcribe = await pipeline(
    "automatic-speech-recognition",
    "Xenova/whisper-small"
)

const transcription = await transcribe(audio, {
    chunk_length_s: 30,
    stride_length_s: 5,
    language: "portuguese",
    task: "transcribe",
})

return transcription?.text.replace("[Música]","")
-->


OBS - bug: Conecções instáveis (uso de WIFI) fará com que perca a conecção com os servidores transformers.js e abortará o processo reiniciando o servidor.

