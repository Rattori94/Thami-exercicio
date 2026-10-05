# LipeFitness

App simples (HTML/CSS/JS puro, sem backend) com o treino adaptado — duas abas:

- **Treino**: alterna entre **Superior** e **Inferior**, cada um com aquecimento rápido + 5 exercícios principais em máquina, botão **"Saber mais"** (execução, músculo, dica para lipedema e vídeo) em cada exercício, e um botão **"Concluir treino de hoje"**.
- **Cardio**: cronômetro para o exercício aeróbico (elíptico/bike), com presets de 20/30/40 min e registro das sessões feitas.

Tudo é salvo no próprio iPhone (localStorage) — não precisa de internet depois de instalado, nem de conta/login.

## Como publicar no GitHub Pages (gratuito)

1. Crie uma conta no [github.com](https://github.com) se ainda não tiver.
2. Crie um novo repositório (ex: `lipefitness-app`), público.
3. Envie estes arquivos para o repositório (pela interface web do GitHub, arrastando os arquivos, ou via linha de comando):

   ```bash
   cd lipefitness-app
   git init
   git add .
   git commit -m "App LipeFitness"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/lipefitness-app.git
   git push -u origin main
   ```

4. No repositório, vá em **Settings → Pages**.
5. Em "Branch", selecione `main` e a pasta `/ (root)`, depois clique em **Save**.
6. Em alguns minutos seu app estará disponível em:
   `https://SEU-USUARIO.github.io/lipefitness-app/`

## Como instalar no iPhone (adicionar à tela de início)

1. Abra o link do app (`https://SEU-USUARIO.github.io/lipefitness-app/`) no **Safari** do iPhone (precisa ser o Safari, não funciona pelo Chrome).
2. Toque no ícone de **compartilhar** (quadrado com seta para cima).
3. Role e toque em **"Adicionar à Tela de Início"**.
4. Confirme o nome "LipeFitness" e toque em **Adicionar**.

Pronto — o app aparece como um ícone normal na tela do iPhone, abre em tela cheia (sem barra do Safari) e funciona offline.

## Estrutura dos arquivos

```
lipefitness-app/
├── index.html         (app completo: HTML + CSS + JS)
├── manifest.json       (configuração do app/ícone para instalação)
├── service-worker.js   (permite funcionar offline)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Personalizar o treino

Os exercícios ficam no início do `<script>` dentro de `index.html`, no objeto `EXERCISES` (listas `superior` e `inferior`). Basta editar nome, séries, descanso etc. diretamente ali — não precisa de nenhuma ferramenta especial, só um editor de texto.

## Sobre a seleção dos exercícios

Cada treino (Superior e Inferior) tem um aquecimento rápido (não conta na meta) seguido de exatamente **5 exercícios principais, 100% em máquinas/cabos guiados** (puxada, remada, supino máquina, cadeira extensora, leg press, cadeira adutora etc.), montados a partir dos treinos originais enviados (ONFIT / LIPEFITNESS). Isso não substitui orientação de um profissional de educação física — ajuste cargas e progressão conforme a orientação de quem acompanha seu treino.

## Botão "Saber mais"

Cada exercício tem um botão **Saber mais** que abre um painel com: grupo muscular trabalhado, como executar o movimento, erro comum a evitar, uma dica adaptada para quem tem lipedema, e um botão para assistir a um vídeo de demonstração selecionado (abre no YouTube — precisa de internet nesse momento; o resto do app continua funcionando offline normalmente).
