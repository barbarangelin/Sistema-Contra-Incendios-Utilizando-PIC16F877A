# Sistema contra incendios utilizando PIC16F877A
Este projeto foi desenvolvido para a disicplina de MICMIC. O objetivo desse projeto é a elaboração de um sistema que realize medições, mudanças na configuração da temperatura e a liberação de sprinkle (servo motor) em caso de incêndio confirmado.
Além disso, foi usado a linguagem C, MikroC para a compilação do código do programa e o Proteus para a simulação

# ${\color{red}Observações}$
No projeto do Proteus foi usado bibliotecas externas, como a do [gas sensor](https://www.theengineeringprojects.com/2016/05/gas-sensor-library-proteus.html).
A lógica para a decisão de se há incêndio ou não é a seguinte:
- Sem fumaça e temperatura dentro do limite: ${\color{pink}cenário \ normal}$
- Sem fumaça porém com temperatura acima do limite:  ${\color{pink}cénario \ de \ calor \ excessivo,\ é \ disparado \ o \ alarme}$
- Com fumaça porém com temparatura abaixo do limite:  ${\color{pink}cénario \ de \ fumaça \ existente,\ é \ disparado \ o \ alarme}$
- Com fumaça e com temperatura acima do limite:  ${\color{pink}indicativo \ de \ incendio, \ é \ disparado \ o \ alarme \ e \ o \ servo \ motor \ (sprinkle)}$


# ${\color{red}Esquemático}$
<img width="1130" height="795" alt="image" src="https://github.com/user-attachments/assets/8404d7ef-e1a5-4042-8cea-3270a9011356" />

# ${\color{red}Sobre \ o \ código \ fonte \ e \ a \ simulação}$
O presente projeto foi concebido dentro de uma semana. Por conta disso, o código fonte acabou sujo. Contudo, há um interesse em melhorar o que já foi feito.
Vale ressaltar que para a simulação ocorrer bem é necessário ter o hex code baixado e então colocar o diretório do arquivo dentro da caixa file na configuração do PIC16F877A.
