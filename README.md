# Sessões de trabalho & priorização RICE — protótipo

Demonstração pública, viva no navegador, de dois sistemas que desenhei no trabalho: um rastreador de sessões de trabalho (iniciar / pausar / retomar / concluir) que mede tempo dedicado e custo estimado por projeto e por pessoa, e um framework de priorização RICE (Alcance × Impacto × Confiança ÷ Esforço) para ordenar um backlog técnico por valor gerado.

Este repositório não reproduz nenhum sistema interno de empresa alguma — é uma recriação genérica, com dados fictícios, construída para portfólio. Tudo roda localmente no navegador (localStorage); nada é enviado a servidor algum.

## Ver a demonstração ao vivo

https://poliana-betella.github.io/gestao-sessoes-rice-demo/

## O que este protótipo mostra

Controle de sessão por estado (não iniciado / em andamento / pausado / concluído), com acúmulo correto de tempo entre pausas e retomadas. Custo estimado por projeto e por analista, a partir de um valor de hora configurável. Backlog priorizado automaticamente por score RICE, recalculado a cada item adicionado.

## Stack

HTML, CSS e JavaScript puro (sem frameworks, sem backend) — propositalmente simples, para deixar a lógica visível.

## Contexto

Autoria de um framework de priorização (RICE) documentado e aplicado para ordenar o backlog técnico de projetos por valor gerado, e desenho de um sistema de sessões de trabalho para medir tempo dedicado por projeto e por pessoa, usado como base para análise de custo operacional. Mais sobre isso em [poliana-betella.github.io/homepage](https://poliana-betella.github.io/homepage/#atuacao).
