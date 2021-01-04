#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#define SIZE 200

char nome[SIZE][50]; 
char email[SIZE] [50];
int cpf[SIZE]; 
int op;

 //aquii sao os metodos  de cadastro e busca
void cadastro(); 
void pesquisa();
void lista();
//fim de metodos 


int main (void){
	//aqui fiz o chamado da funcao no sistema
	
	do{
		system("cls");
		printf(" *******SEJA BEM VINDO******* \n\n");
		printf("|-------MENU PRINCIPAL-------|  \n");
		printf("| 1 |- Cadastrar                \n");
		printf("| 2 |- pesquisar                \n");
		printf("| 3 |- listar todos             \n");
		printf("| 4 |- Sair                     \n");
		scanf("%d", &op);
		switch(op){
			case 1: 
				cadastro();
				break;
			case 2:
				pesquisa();
				break;
			case 3:
				lista();
				break;
			case 4: 
				system("exit");
				break;	
				
			default:
				printf("Opcao invalida[!]");
				break;
		}
		
		}while(op!=4);
} 
//inicio da funcao listar
void lista(){
	int i; 
	for(i=0;i<SIZE;i++) {
		if(cpf[i]>0){
			printf("\nNOME: %s\nE-MAIL: %s\nCPF: %d", nome[i], email[i], cpf[i] );
		} else { 
		break;
		}
	
	}
	getchar();
}; // fim da funcao lista
//inico da funcao de cadastro
void cadastro(){
	static int linha;
	do{ 
		printf("\nDigite o NOME...: ");	
		scanf("%s", &nome[linha]);
		printf("\nDigite o E-MAIL...:");
		scanf("%s", &email[linha]);
		printf("\nDigite o CPF...: ");
		scanf("%d", &cpf[linha]); 
		printf("\n| 1 |-Seguir | 0 |- sair..:");
		scanf("%d", &op);
		linha++;
		
	}while(op==1);
} //fim da funcao 
//comeco da funcao pesquisa
void pesquisa(){
	int cpfPesquisa;
	int i ;
	char emailPesquisa[50];
	do{
		printf("\nDigite| 1 |- para cpf ou | 2 |para E-mail...:");
		scanf("%d", &op);
		switch(op) {
			case 1:
				printf("\nDigite o CPF: ");
				scanf("%d", &cpfPesquisa);
				for(i=0;i<SIZE;i++){
					if(cpf[i]==cpfPesquisa) {
						printf("\nNOME: %s\nE-MAIL: %s\nCPF: %d", nome[i], email[i], cpf[i] );
							}
				}
				break;
			case 2:
				printf("\nDigite o E-MAIL: ");
				scanf("%s", emailPesquisa);
				for(i=0;i<SIZE;i++){
					if(strcmp(email[i], emailPesquisa)){
						printf("\nNOME: %s\nE-MAIL: %s\nCPF: %d", nome[i], email[i], cpf[i] );
					}
				}
				break;
				
			default:
			printf("opcao invalida [!]");
				break;	
		}
		printf("\nDigite | 1 |- para continuar pesquisa");
		scanf("%d", &op); 
	
	
	}while(op==1);
	
}  //fim da funcao pesquisa
