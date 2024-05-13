importar java.util.Random;
importar javax.swing.JOptionPane;
classe pública TrabalhoFinal {

public static void main(String[] args) {
        // Lógica de aplicação do código TODO aqui
        //declaração de vetores
        int vetx[] = novo int[10];
        int vety[] = new int[10];
        int vetz[] = novo int[10];
        booleano vetb[] = novo booleano[31];


        //declaração de strings
        String nome1 = "", nome2 = "", nome3 = "";
        Sequência x = "";
        String y = "";
        String z = "";

        //declaração das demais variáveis        
        int pta = 0, ptb = 0, ptc = 0, i = 0, op;
        Aleatório r = novo Aleatório();
        sinalizador booleano = falso;

        //Apresentação
        JOptionPane.showMessageDialog(null, "WM ENTERPRISE TECHNOLOGY\n"
        +"apresenta");
        JOptionPane.showMessageDialog(null,"SUPER BINGO PROG I - v1.3");


        //cardápio
        fazer {

            op = Integer.parseInt(JOptionPane.showInputDialog(null, "Escolha uma opção abaixo:\n1 - Jogar\n2 - Instruções\n0 - Sair"));

            mudar (operar) {
                caso 0:
                    JOptionPane.showMessageDialog(null, "Obrigado por jogar!");
                    continuar;
                caso 2:
                    JOptionPane.showMessageDialog(null, "Entre com o nome do jogador e os números de 1 a 30, sem repetir;\n"
                                                        + "Faça isso para os três jogadores,logo após o início do sorteio;\n"
                                                        + "Boa sorte e divirta-se!!!");
                    continuar;
                caso 1:

                    //preenchimento da primeira cartela
                    nome1 = missão();
                    preencherCartela(vetx);
                    for (int cont = 0; cont < vetx.length; cont++) {
                        x += vetx[cont] + " / ";
                    }

                    //preenchimento da segunda carta
                    nome2 = missão();
                    preencherCartela(vety);
                    for (int cont = 0; cont <vety.length; cont++) {
                        y += vety[cont] + " / ";
                    }

                    //preenchimento da terceira carta
                    nome3 = missão();
                    preencherCartela(vetz);
                    for (int cont = 0; cont <vetz.length; cont++) {
                        z += vetz[cont] + " / ";
                    }

                    //mostra as castelas preenchidas
                    JOptionPane.showMessageDialog(null, "BOA SORTE!!!\n" + nome1 + " - " + x + "\n" + nome2 + " - " + y + "\n" + nome3 + " - " + z + "\n");
            }
            //sorteio dos números
            while (sinalizador == falso) {
                int classificação = r.nextInt(30) + 1;
                eu = classificar;

                if (vetb[i] == falso) {

                    //mostra o número sorteado
                    JOptionPane.showMessageDialog(null, "O número sorteado foi o número " + sorte +" !");
                    vetb[i] = verdadeiro;
                } outro {
                    continuar;
                }

                //verifica quais cartelas possuem o número sorteado
                for (int cont = 0; cont < vetx.length; cont++) {
                    if (vetx[cont] == ​​classificar) {
                        pta++;

                        se (pta == 10) {
                            bandeira = verdadeiro;
                            bingo(nome1);
                            quebrar;
                        }
                    }
                    if (vety[cont] == ​​classificar) {
                        ptb++;

                        if (ptb == 10) {
                            bandeira = verdadeiro;
                            bingo(nome2);
                            quebrar;
                        }
                    }
                    if (vetz[cont] == ​​classificar) {
                        ptc++;

                        if (pt == 10) {
                            bandeira = verdadeiro;
                            bingo(nome3);
                            quebrar;
                        }
                    }
                }
                //mostra qual a cartela que possui o número sorteado
                JOptionPane.showMessageDialog(null,"( "+ nome1 + ") - " + x + " Certos["+pta+"]\n\n"
                                                  +"( "+ nome2 + ") - " + y + " Acertos["+ptb+"]\n\n"
                                                  +"( "+ nome3 + ") - " + z + " Acertos["+ptc+"]");
            }
            x = ""; z = ""; y = "";
        } enquanto (op! = 0);

    }

    public static void bingo(String ganha) {
        JOptionPane.showMessageDialog(null, "BINGO!!!\n"
        +"O jogador " + ganhou + " foi o grande ganhador!!!");
        JOptionPane.showMessageDialog(null, "Parabéns " + ganhou + ",o seu prêmio é um joinha!!!");
    }


    public static void preenchimentoCartela(int v[]){



        int numIgual;
        validação booleana;
        String cartela="";
        fazer {
            numIgual = 0;
            for (int i = 0; i < v.comprimento; i++) {

                fazer {

                    valido = verdadeiro;
                    v[i] = Integer.parseInt(JOptionPane.showInputDialog(null, "Digite o seu " + (i + 1) + "º valor da cartela:\n"+cartela));

                    se (v[i] > 30 | v[i] == 0) {
                        JOptionPane.showMessageDialog(null, "Coloque um número válido!");
                        valido = falso;

                    }

                } while (valido == falso);
                //não permite números fora do limite permitido
                carta +=v[i]+" / ";
            }

            for (int i = 0; i < 9; i++) {
                for (int j = 1; j < v.comprimento; j++) {

                        se (v[i] == v[j]){
                            se(eu!=j){
                                numIgual++;
                            }
                        }

                }
            }
            if (numIgual! = 0) {
                JOptionPane.showMessageDialog(null,"Não vale colocar números iguais!");
                cartela="";
            }

        } while (numIgual! = 0);
        //não permite números repetidos
    }

    public static String busca() {
        String jogador = "";
        Aleatório r = novo Aleatório();
        int pergunta = r.nextInt(8);
        switch (pergunta) {
            caso 0:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "Digite logo seu nome, não me faça perder tempo: "));
                quebrar;
            caso 1:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "Não quero papo com você, digite logo seu nome: "));
                quebrar;
            caso 2:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "Uau gostei de você, que tal um açaí depois do jogo? Qual é o mesmo seu nome: "));
                quebrar;
            caso 3:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "Leu as regras?? Digite seu nome: "));
                quebrar;
            caso 4:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "vamos testar sua classificação, digite seu nome: "));
                quebrar;
            caso 5:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "Agradeça aos caras que me programaram por estar jogando isso, digite seu nome: "));
                quebrar;
            caso 6:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "Contas para pagar? Vamos tentar ganhar um dinheiro, digite seu nome: "));
                quebrar;
            caso 7:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "Soube que você precisa de dinheiro para casar, tente sortear aqui. Digite seu nome: "));
                quebrar;
            caso 8:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "Você não pode ser um jogador de sorte, mas digite seu nome: "));
                quebrar;
            caso 9:
                jogador = String.valueOf(JOptionPane.showInputDialog(null, "Ouvi falar que você é um cara sem sorte, mas vou deixá-lo jogar, qual seu nome: "));
        }
        retornar jogador;
    }
}
