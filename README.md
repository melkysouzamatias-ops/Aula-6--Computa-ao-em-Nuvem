# Aula-6--Computa-ao-em-Nuvem

# Aula 6 — Kubernetes e Persistência de Dados

## 1. O que fizemos na aula?

Nesta aula, criamos uma página web com Nginx usando um ConfigMap e aprendemos a armazenar arquivos no Kubernetes utilizando PV e PVC.

Também testamos se os arquivos continuavam salvos depois de excluir um Pod e criar outro.

## 2. Erros que cometi

- Errei a indentação dos arquivos YAML, fazendo com que o Kubernetes não reconhecesse os recursos.
- Coloquei dois-pontos a mais no campo `ReadWriteOnce` do PVC.
- Tentei executar comandos em Pods que não tinham sido criados.
- Errei a sintaxe do comando `sed` ao tentar criar outro arquivo YAML.
- Precisei configurar um PV para que o PVC tivesse um armazenamento disponível.

## 3. O que corrigimos?

Corrigimos a indentação dos arquivos, ajustamos os comandos e configuramos o armazenamento corretamente.

Depois, criamos os Pods, salvamos os arquivos `mensagem.txt` e `grupo.txt` e excluímos um dos Pods para testar se os dados continuavam disponíveis.

## 4. O que aprendemos?

- ConfigMap: guardar configurações, como o conteúdo de uma página HTML.
- Pod: executar aplicações no Kubernetes.
- PV e PVC: disponibilizar e solicitar armazenamento.
- Persistência: manter os arquivos salvos mesmo depois de excluir um Pod, utilizando o mesmo volume persistente.

## 5. Conclusão

A aula foi importante para aprender a criar Pods, corrigir erros nos arquivos YAML e trabalhar com armazenamento no Kubernetes. O principal aprendizado foi entender que podemos excluir e recriar um Pod sem perder os dados que estão salvos em um volume persistente.
