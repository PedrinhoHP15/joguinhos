//# joguinhos
//3 jogos, olho de cobra, adivinhe o numero e perguntas.









#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <time.h>
#include <locale.h>

//pedro belchior damasceno de almeida: 22300022
//github===PedrinhoHP15
int main()
{
setlocale(LC_ALL, "Portuguese"); 
	srand(time(NULL));
int menu;
char resposta; 
int nivel;
int certo_1=0,errado_1=0; //defeinir pelo codigo certo e errado
int answer = -1;
int guess = 0;               
int count = 6; //numero sorteado
int chosen;
srand(time(0));
chosen=rand()%1000;// printf("%d", chosen);
int cobra;//menu do olho de cobra

	do
	{
		
	    printf("\n~~~~BEM VINDO AOS JOGOS~~~~\n");
		printf("Olá eu sou Alpha, seu Guia dos Jogos...\n");
		printf("Selecione abaixo quais dos 3 jogos vc quer jogar\n");
		printf("1-jogo das perguntas.\n2-Advinhe o número.\n3-Olho de Cobra.\n");
		printf("4-Sair da sala de jogos\n");
		printf("Selecione qual você deseja?:");
		scanf("%d", &menu);
		system("cls");
		switch(menu)
		{
		case 0:
		printf("\n~~~~BEM VINDO AOS JOGOS~~~~\n");
		printf("Olá eu sou Alpha, seu Guia dos Jogos...\n");
		printf("Selecione abaixo quais dos 3 jogos vc quer jogar\n");
		printf("0-Menu\n1-jogo das perguntas.\n2-Advinhe o número.\n3-Olho de Cobra.\n");
		printf("4-Sair da sala de jogos\n");
		printf("Selecione qual você deseja?:");
		scanf("%d", &menu);
		system("cls");
		// ----------------JOGO DE PERGUNTAS -----------------------------------
		case 1:
			do
			{
	printf("\n<><><><><><><BEM VINDO AO JOGO PERGUNTAS E RESPOSTAS.><><><><><><><>\n");
	printf("\nEu sou Alpha, guiarei você as proximas perguntas.\n");
	printf("Selecione qual desafio de pergunta vc quer:\n "); 
	printf("\n\t1- Desafio muito fácil:"); 
	printf("\n\t2- Desafio fácil: ");
	printf("\n\t3- Desafio médio: ");
	printf("\n\t4- Desafio difícil: ");
	printf("\n\t5- Sair do jogo.");
	printf("\nAlpha- Escolha a proxima pergunta: ");
	scanf("%d", &nivel);
	
		switch(nivel)
		
	{
	case 1: //esse é o primeiro desafio 
		system("cls"); //reiniciar o programa pra 
		printf("Alpha- esse é o desafio muito fácil, não vá errar...\n");
		printf("Alpha- O que, o que tem coroa mas nao e rei?\n");
		printf("\ta)Moeda\n\tb)Abacaxi\n\tc)Caneta\n");
		printf("qual é a resposta? ");
		scanf("%s", &resposta);
		
		if ((resposta =='B')||(resposta =='b'))
		{
			printf("\nAlpha- parabéns!Você acertou!\n\n");
			certo_1++;
		}
		else
		{
			printf("\nAlpha- Desculpe você errou...\n");
			printf("\nA resposta certa era a \"B\"\n\n");
			errado_1++;
		}
		break;
	
	case 2:  //esse é o segundo desafio 
		system("cls");
		printf("Alpha- esse é o desafio fácil, não vá errar...\n");
		printf("Alpha- O que é feito pra andar, mas não  anda?\n");
		printf("\ta)Pé\n\tb)Roda\n\tc)Rua\n");
		printf("qual é a resposta? ");
		scanf("%s", &resposta);
		
		if ((resposta =='C')||(resposta =='c'))
		{
			printf("\nAlpha- parabéns!Você acertou!\n\n");
			certo_1++;
		}
		else
		{
			printf("\nAlpha- Desculpe você errou...\n");
			printf("\nA resposta certa era a \"C\"\n\n");
			errado_1++;
		}
		break;
	
	case 3: //terceiro desafio
		system("cls");
		printf("Alpha- Essa é Média, Boa sorte!\n");
		printf("Alpha- O que é, o que é vai para cima e para baixo sem sair do lugar? \n");
		printf("\ta)Escada\n\tb)Elevador\n\tc)Cabeça\n");
		printf("qual é a resposta? ");
		scanf("%s", &resposta);
		
		if ((resposta =='A')||(resposta =='a'))
		{
			printf("\nAlpha- parabéns!Você acertou!\n\n");
			certo_1++;
		}
		else
		{
			printf("\nAlpha- Desculpe você errou...\n");
			printf("\nA resposta certa era a \"A\"\n\n");
			errado_1++;
		}
		break;
	case 4: //quarto desafio
		system("cls");
		printf("Alpha- Essa é difícil, nem eu sei a resposta\n");
		printf("Alpha- O que é, o que é Nunca Volta, embora nunca tenha ido?\n");
		printf("\ta)O passado\n\tb)O amor\n\tc)A saudade\n");
		printf("qual é a resposta? ");
		scanf("%s", &resposta);
		
		if ((resposta =='A')||(resposta =='a'))
		{
			printf("\nAlpha- parabéns!Você acertou!\n\n");
			certo_1++;
		}
		else
		{
			printf("\nAlpha- Desculpe você errou...\n");
			printf("\nA resposta certa era a \"A\"\n\n");
			errado_1++;
		}
		
		break;
	case 5: //função para sair do jogo
	
		system("cls");
				printf("\nAperte 0 para voltar ao menu de jogos\n");
				scanf("%d", &menu);
				break;
			default:
				printf("\nOpcao nao reconhecida, verifique o codigo informado.\n");
				system("cls");
				break;
			}
	}while(nivel != 5);
	break;

	//-------------------JOGO DE ADVINHE O NUMERO------------------------------------------------
		case 2:
   while(answer != 4)
   {
   	setlocale(LC_ALL, "Portuguese");
        printf("------------------------------------------------------------------------------\n");
	printf("\tBEM VINDO AO JOGO:ADVINHE O NÚMERO\n");
	printf("     Alpha- Tente advinhar o número sorteado!\n");
	printf("-------------------------------------------------------------------------------\n");
	
	printf("-REGRA- Você terá apenas 5 Tentativas para acertar um número de 0 ate 1000\n");
	printf("Alpha- Preparado? caso esteja pronto, começe!\n");
        
        printf("1 - Comecar jogo?\n");
        printf("2 - sair?\n");
        printf("Escolha: \n");
        scanf("%d", &answer);
        
        switch(answer)
		{
              case 1:
                  for(count > 0; --count;){
                  printf("\nAlpha- Voce tem %d tentativas restantes.", count);
                  printf("\nDigite um número: ");      
                  scanf("%d", &guess);              

                  if(guess == chosen){
                    printf("\nAlpha- Parabéns, você acertou!\n");
                                 
     
                  }else if(guess < 1 || guess > 1000)  
                    printf("O número escolhido não está entre o 0 e 1000.\n ");
                          else
                              printf("Errou!, %d não está correto. O número sorteado %s que o número escolhido.\n", guess, chosen > guess ? "MAIOR" : "MENOR");
   
                  }
   
                  printf("\nExcedeu as 5 tentativas, o número sorteado era: %d\n\n", chosen);
                     
                  break;
                  
              case 2:
			  printf("\nAperte 0 para voltar ao menu de jogos\n");
			  scanf("%d", &menu);
				break;
		          default:
                     printf("\nComando invalido\n");    
                     break;
			 }
			 break;
			 }
			 break;
		 //------------------------OLHO DE COBRA---------------------------------
		 case 3:
		do{ 		
	printf("~~~~~~~~OLHO DE COBRA~~~~~~~~\n");
	printf("         ,,'6''-,.\n");
	printf("        <====,.;;--.\n");
	printf("        _`---===. ""==__\n");
	printf("      //""@@-\===\@@@@ ""\\\n");
	printf("     |( @@@  |===|  @@@  ||\n");
	printf("      \\ @@   |===|  @@  //\n");
	printf("        \\ @@ |===|@@@ //\n");
	printf("         \\  |===|  //\n");
	printf("___________\\|===| //_____,-----------------,_\n");
	printf("  -------,__`\===`/ _________,---------,____   `,\n");
	printf("             |==||                           `\ \ \n");
	printf("            |==| |                             ) |\n");
	printf("           |==| |       _____         ______,--' /  '\n");
	printf("           |=|  --------     ---------         /   \n");
	printf("           \=\     __,------------------------ \n"); 
	printf("            \=\------\n");
	printf("OLÁ EU SOU O ALPHA, BEM VINDO AO JOGO\n");
	printf("Selecione as opções abaixo o que você deseja.");
	printf("\n\t1- Regras do jogo");
	printf("\n\t2- Jogar!!");
	printf("\n\t3- Sair");
	printf("\nSelecione um dos numeros: ");
	scanf("%d", &cobra);
	
	switch(cobra)
	{
	case 1:
		system("cls");
		printf("Alpha-O jogo precisa de 2 jogadores, onde cada 1 terá um turno\n");
		printf("dentro do seu turno o jogador tem as opcoes de: \n");
		printf("pular seu turno, ou jogar os dados novamente.\n");
		printf("\nAo escolher jogar os dados de novo, a soma desses \n");
		printf("valores sera acrescentado a sua pontuacao, porem o jogador tem dois riscos!\n");
		printf("Alpha-O primeiro: se em um dado cair o valor 1.\n o jogador perde todos os pontos acumulados\ne perde a sua vez\n");
		printf("Alpha-O segundo: Se os dois dados cairem 1, o jogador perde todos os pontos que ganhou durante o jogo");
		printf("para zero, e perde sua vez. \n digite 2 para jogar o jogo.\n");
		scanf("%d", &cobra);
		system("cls");
		break;
	case 2:
char nome1[15];
char nome2[15];
int game = 1;      
int dado1 = 0;
int dado2 = 0;
int dado3 = 0;
int dado4 = 0;
int vj1 = 0;
int vj2 = 0;
int jogador = 0;
jogador = rand() % 2;
system("cls");
printf("Alpha-Bem vindo ao jogo olho de cobra, Selecione os seus nicknames a baixo.\n");
printf("Seu nome 1: ");gets(nome1);
scanf("%s", &nome1);
printf("Seu nome 2: ");gets(nome2);
scanf("%s", &nome2);

    while(game == 1){
    	system("cls");
        	if(jogador == 0){
				printf("Turno do %s: ", nome1);
			}
			else if(jogador == 1)
			{
				printf("Turno do %s: ", nome2);
			}
            switch (jogador) {
                case 0:
                    if (vj1 >= 50) {
                    	
					printf("Jogador %s Ganhou!\n seu valor total: %d", nome1, vj1);
					game = 0;
					vj1 = 0;
					jogador = 0;
					system("cls");
					break;
                    }
                    if (dado1 == 1 || dado2 == 1) {
					dado1 = rand() % 6 + 1;
					dado2 = rand() % 6 + 1;
                    	printf("\nface do dado UM: %d\n face do dado DOIS: %d\n", dado1, dado2);
                        printf("Uma das suas faces deu 1.\n Logo vc perde os pontos e seu turno.");
						jogador = 1;
                    }else if (dado1 == 1 && dado2 == 1) {
                    	printf("\nface do dado UM: %d\n face do dado DOIS: %d\n", dado1, dado2);
                    	printf("Você acertou o olho de cobra.\n Perdeu todos os seus pontos acumulados.\n");
                    	printf("Digite 0 para continuar\nDigite 1 para trocar o turno com oponente.\n");
                        scanf("%d", &jogador);
                        vj1 = 0;
                        break;
                        
                    }else if(dado1 > 1 && dado2 > 1)
					 {
                        vj1 += dado1 + dado2;
						printf("Turno do %s.\n", nome1);
                        printf("\nface do dado UM: %d\n face do dado DOIS: %d\n", dado1, dado2);
                        printf("Total de pontos de %s: %d\n", nome1, vj1);
                        printf("\nTotal de pontos de %s: %d\n", nome2, vj2);
                        printf("Digite 0 para continuar\nDigite 1 para trocar o turno com oponente.\n");
                        scanf("%d", &jogador);
                        break;
                    }
                case 1:
                    dado3 = rand() % 6 + 1;
                    dado4 = rand() % 6 + 1;
                    if (vj2 >= 50) {
                      printf("Jogador %s Ganhou!\n seu valor total: %d", nome2, vj2);
					  game = 0;
					  vj2 = 0;
					  jogador = 0;
                    }
                     if (dado3 == 1 || dado4 == 1) {
                    	printf("\nface do dado UM: %d\n face do dado DOIS: %d\n", dado3, dado4);
                        printf("Uma das suas faces deu 1.\n Logo vc perde os pontos e seu turno.");
                        jogador = 0;
                        
                    }else if (dado3 == 1 && dado4 == 1) {
                    	printf("\nface do dado UM: %d\n face do dado DOIS: %d\n", dado3, dado4);
                    	printf("Você acertou o olho de cobra.\n Perdeu todos os seus pontos acumulados.\n");
                    	printf("Digite 0 para continuar\nDigite 1 para trocar o turno com oponente.\n");
                        scanf("%d", &jogador);
                        vj2 = 0;
                        break;
                    } if(dado3 > 1 && dado4 > 1)
					 {
                        vj2 += dado3 + dado4;
                        printf("Turno do %s.\n", nome2);
                        printf("\nface do dado UM: %d\n face do dado DOIS: %d\n", dado3, dado4);
                        printf("Total de pontos de %s: %d\n", nome1, vj1);
                        printf("\nTotal de pontos de %s: %d\n", nome2, vj2);
                        printf("Digite 1 para continuar\nDigite 0 para trocar o turno com oponente.\n");
						scanf("%d", &jogador);
						break;
					
                    }
                    break;
            }
        }
        	break;
}
		}while(cobra !=3);

case 4:
	printf("Alpha- Deseja voltar ao menu?\nAperte<1>\n Se deseja parar de jogar\n Aperte<5>");
	printf("\nSelecione: ");
	scanf("%d", &menu);   

	break;

	default:
	printf("###opção invalida! use a opção valida!###");
	break;
	}
}while(menu != 5); 
    }
 
