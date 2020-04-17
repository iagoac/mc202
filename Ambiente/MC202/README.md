#3

Se chegou até aqui, então todo o seu ambiente já está devidamente configurado, ou pelo menos deveria estar. Tudo o que você precisa fazer agora é codificar.

##LINUX

Comandos básicos Linux: **https://maker.pro/linux/tutorial/basic-linux-commands-for-beginners**

##NO AMBIENTE CONFIGURADO

1) Abra o terminal na pasta **MC202** após sua extração. Quando estiver dentro da pasta clique com o **botão direito** e selecione "**Abrir terminal aqui**".

2) No terminal utilize o comando "**make preparar_ambiente PDF=1 LAB=01 MAX_TST=6**", sendo:
	- **PDF** -> o número do lab ao qual se refere
	- **LAB** -> o número do lab ao qual se refere, mas com necessariamente 2 digitos
	- **MAX_TST** -> o número do ultimo teste aberto disponível no Susy

   Dessa forma o **Atom** se abrirá na nova pasta do lab com:
	- O **PDF** do lab
	- Um **arquivo .c** com uma main já definida
	- Um **Makefile** já configurado, será explicado mais para baixo como utiliza-lo
	- Todos os **testes** do Susy já baixados.

3) Codifique tudo como o PDF do Lab orienta.

##NO TERMINAL NA PASTA DO LAB A SER DESENVOLVIDO

4) Para **gerar o executável** do seu programa basta utilizar o seguinte comando "**make build LAB=01**", sendo:
	- **LAB** -> o número do lab ao qual se refere, mas com necessariamente 2 digitos

5) Para **testar suas saidas** com as esperadas pelo Susy utilize "**make testar_programa LAB=01**", sendo:
	- **LAB** -> o número do lab ao qual se refere, mas com necessariamente 2 digitos

6) Para **validar erros de MEMORY LEAK** entre outros erros comuns, utilize "**make checar_testes LAB=01**", sendo:
	- **LAB** -> o número do lab ao qual se refere, mas com necessariamente 2 digitos

OBS:  Caso tenha **deletado os testes** sem querer basta rodar o seguinte comando: "**make baixar_testes LAB=01 MAX_TST=6**", sendo:
	- **LAB** -> o número do lab ao qual se refere, mas com necessariamente 2 digitos
	- **MAX_TST** -> o número do ultimo teste aberto disponível no Susy

OBS:  Caso tenha **deletado o PDF** sem querer basta rodar o seguinte comando: "**make baixar_pdf PDF=1**", sendo:
	- **PDF** -> o número do lab ao qual se refere

Se tudo tiver passado com os **RESULTADOS CORRETOS**, já **pode mandar sua solução** para o Susy :)


----------------------------------------------------------------------------------------------------

Qualquer dúvida exitente é só me chamar!

Emilio de Oliveira Costa - CC019
11 972305012
