
 Gerador de URL RTSP (RTSP URL Generator)

Este é um script utilitário simples em Python (CLI) projetado para resolver um problema comum: a dificuldade em montar a URL de streaming RTSP correta para diferentes marcas de câmeras de segurança, DVRs e NVRs.

O formato da URL RTSP pode variar significativamente entre fabricantes. Este utilitário serve como um assistente de linha de comando que guia o usuário através do processo, solicitando as informações necessárias (como IP, porta, usuário, senha) para montar a URL final corretamente.

 Funcionalidades

* **Interface Interativa (CLI):** Um menu simples para selecionar a marca e preencher os dados.
* **Modelos (Templates) Prontos:** O script armazena os formatos de URL específicos para cada marca.
* **Textos de Ajuda:** Guia o usuário sobre o que cada campo significa (ex: "subtype 0 para stream principal").
* **Fácil de Expandir:** Adicionar novas marcas é tão simples quanto adicionar uma nova entrada ao dicionário `MARCAS`.

 Marcas Suportadas (Atualmente)

* Intelbras
* Hikvision
* Uniview (UNV)

Como Usar

1.  Certifique-se de ter o [Python 3](https://www.python.org/downloads/) instalado em seu sistema.
2.  Faça o download ou clone o script.
3.  Abra seu terminal ou prompt de comando.
4.  Navegue até a pasta onde o script está e execute-o:

    ```bash
    python nome_do_script.py
    ```

5.  O menu interativo será exibido:

    ```
    ===== Gerador de URL RTSP =====
    [1] - Intelbras
    [2] - Hikvision
    [3] - Uniview (UNV)
    [0] - Sair
    ===============================
    Escolha o número da marca desejada:
    ```

6.  Siga as instruções, preencha os campos solicitados e a URL RTSP final será gerada na tela.

 Como Contribuir

Sinta-se à vontade para contribuir com mais marcas de câmeras! O processo é simples:

1.  Faça um "Fork" deste repositório.
2.  Edite o script e adicione a nova marca ao dicionário `MARCAS` no início do arquivo. Siga o formato existente:

    ```python
    "nova_marca": {
        "nome_exibicao": "Nome da Nova Marca",
        "template": "rtsp://formato-da-url/{USUARIO}@{DOMINIO}...",
        "ajuda": {
            "USUARIO": "Dica para o usuário",
            "DOMINIO": "Dica para o domínio",
            # ... outros campos
        }
    },
    ```

3.  Abra um "Pull Request" com suas mudanças.
