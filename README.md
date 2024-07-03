# Como configurar/instalar o `PlotDigitizer` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar o `PlotDigitizer` no Linux Ubuntu.

## _Abstract_

_In this document are contained the main commands and settings to set up/install the `PlotDigitizer` on `Linux Ubuntu`._

## Descrição [2]

### `PlotDigitizer`

O `PlotDigitizer` é uma ferramenta de código aberto usada para extrair dados numéricos de gráficos ou imagens, permitindo aos usuários digitalizar pontos e valores diretamente a partir de gráficos não digitais, como gráficos impressos ou gráficos em imagens escaneadas. Essa ferramenta é particularmente útil em campos como ciência, engenharia e análise de dados, onde informações precisas são necessárias a partir de figuras ou gráficos não disponíveis em formato de dados tabulares. O `PlotDigitizer` permite que os usuários definam pontos de referência nos eixos do gráfico e, em seguida, selecione pontos de dados diretamente da imagem, gerando um conjunto de valores numéricos correspondentes aos pontos selecionados. Isso economiza tempo e esforço na tarefa de extrair dados de gráficos, tornando-o uma escolha valiosa para aqueles que precisam converter informações visuais em dados quantitativos.

## 1. Como configurar/instalar o `PlotDigitizer` no `Linux Ubuntu` [1]

Para configurar o `PlotDigitizer`, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`



2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

3. **Navegue até o diretório onde o arquivo `.deb` está localizado:** Use o comando cd para navegar até o diretório onde o arquivo `.deb` está localizado. Por exemplo, se o arquivo `.deb` estiver na sua pasta `Downloads`, você pode usar o seguinte comando: `cd ~/Downloads`

4. Instale o arquivo `.deb`: Use o comando `dpkg` para instalar o arquivo `.deb`. Substitua "`<nome_do_arquivo>.deb`" pelo nome real do arquivo `.deb` que você deseja instalar: `sudo dpkg -i plotdigitizer.amd64.deb`

    Você precisará fornecer sua senha de administrador (`sudo`) para continuar.

5. Resolva as dependências (se necessário): Às vezes, a instalação do arquivo `.deb` pode gerar erros devido a dependências ausentes. Se isso acontecer, você pode usar o seguinte comando para tentar resolver as dependências: `sudo apt install -f`

    O comando acima tentará instalar automaticamente as dependências necessárias para o pacote `.deb` que você está instalando.

6. **Verifique a instalação:** Após a conclusão do processo, verifique se o programa ou pacote foi instalado corretamente. Você pode fazer isso procurando o aplicativo no menu de aplicativos ou executando-o a partir do terminal com o comando: `plotdigitizer`

Isso deve permitir que você instale um arquivo `.deb` no seu sistema Ubuntu. Lembre-se de que os arquivos .deb são pacotes de software específicos para distribuições baseadas no Debian, como o Ubuntu, e geralmente são seguros de usar, especialmente se você os obtiver de fontes confiáveis. No entanto, sempre esteja ciente da origem dos arquivos .deb que você baixa e evite fontes não confiáveis para garantir a segurança do seu sistema.


## 2. Código completo para configurar/instalar

Para instalar o `btop` no Linux Ubuntu sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean                                                            
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    cd ~/Downloads
    sudo dpkg -i plotdigitizer.amd64.deb
    sudo apt install -f
    plotdigitizer
    ```


## Referências

[1] OPENAI. ***Instalar arquivo .sh no ubuntu.*** Disponível em: <https://chat.openai.com/c/073320a8-7cc5-4590-9da0-d2bcc7093c88> (texto adaptado). Acessado em: 17/10/2023 16:05.

[2] OPENAI. ***VS code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 14/11/2023 09:33.

