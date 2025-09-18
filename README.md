# Relatório de Atividade

**Nome:** [Pablo Nunes Dias](https://github.com/pndias)
**Data:** 15 de setembro de 2025

---

## Introdução

O objetivo deste exercício é documentar o processo de instalação do docker e criação de uma imagem fedora num container para a execução e documentação de comandos
---

## Relato das Atividades

Para alcançar o objetivo proposto, as seguintes atividades foram realizadas:

1.  **[Atividade 1 - Instalação do docker e comandos de navegação básica]**: Execute o seguinte comando para baixar a imagem do Fedora e iniciar um contêiner interativo:  

```bash
docker run -it --name fedora-tutorial fedora:latest /bin/bash
```

Descrevendo as opções do comando:
- `-it` → Modo interativo  
- `--name fedora-tutorial` → Nome do contêiner  
- `fedora:latest` → Imagem utilizada  

        ![Print do exercício](/images/navegacao-basica.png)

2.  **[Atividade 2 - Manipulação de arquivos]**: Criar, copiar, mover e excluir arquivos, trabalhando com diretórios home e subpastas.  

1. Acesse o diretório home do usuário:
   ```bash
   cd ~
   ```
   - Verifique se está no home:  
     ```bash
     pwd
     ```
2. Crie um arquivo `arquivo1.txt` no diretório home:  
   ```bash
   touch arquivo1.txt
   ```
3. Renomeie o arquivo para `documento.txt`:  
   ```bash
   mv arquivo1.txt documento.txt
   ```
4. Acesse a pasta `atividades` (criada na Atividade 1):  
   ```bash
   cd atividades
   ```
5. Dentro de `atividades`, crie um subdiretório chamado `backup`:  
   ```bash
   mkdir backup
   ```
6. Copie `documento.txt` (do home) para `backup`:  
   ```bash
   cp ~/documento.txt backup/
   ```
   - Verifique se o arquivo foi copiado:  
     ```bash
     ls backup/
     ```
7. Volte ao diretório home usando `cd ~`:  
   ```bash
   cd ~
   ```
   - Confirme o local atual:  
     ```bash
     pwd
     ```
8. Exclua o `documento.txt` original (no home):  
   ```bash
   rm documento.txt
   ```
9. Verifique se o arquivo ainda existe em `backup`:  
   ```bash
   ls atividades/backup/
   ```

        ![Print do exercicio 2](/images/manipulacao-arquivos.png)

3.  **[Atividade 3 - Gerenciamento de Pacotes]**: CInstalar e remover pacotes usando `dnf`.  

1. Atualize a lista de pacotes:  
   ```bash
   dnf update -y
   ```
2. Instale o editor de texto `nano`:  
   ```bash
   dnf install nano -y
   ```
3. Verifique se o `nano` foi instalado:  
   ```bash
   nano --version
   ```
4. Remova o `nano`:  
   ```bash
   dnf remove nano -y
   ```
        ![Exercício 3](/images/gerenciamento-pacotes.png)

---

 **[Atividade 4 - Permissões de arquivo]**: manipular permissões utilizando o comando chmod. 

1. Crie um arquivo `script.sh`:  
   ```bash
   touch script.sh
   ```
2. Dê permissão de execução ao dono:  
   ```bash
   chmod u+x script.sh
   ```
3. Verifique as permissões:  
   ```bash
   ls -l script.sh
   ```

        ![Exercício 4](/images/permissao-arquivo.png)

 **[Atividade 5 - Monitorar e encerrar processos]**: monitorar e encerrar processos através do terminal 

1. Liste processos em execução:  
   ```bash
   ps aux
   ```
2. Execute um processo em segundo plano (ex: `sleep 60`):  
   ```bash
   sleep 60 &
   ```
3. Encontre o **PID** do processo `sleep`:  
   ```bash
   ps aux | grep sleep
   ```
4. Encerre o processo:  
   ```bash
   kill <PID>
   ```

        ![Exercício 4](/images/monitorar-encerrar-processos.png)
