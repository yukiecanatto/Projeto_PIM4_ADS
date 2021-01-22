#include <stdio.h>
#include <string.h>
#include <stdlib.h>



int main ()
{
	//DADOS DO LOGIN E SENHA
    char login[15] = "dr";
    char login1[15];
    char senha[15] = "picapau";
    char senha1[15];


    printf("LOGIN: ");
    scanf("%s",login1);
    printf("\nSENHA:");
	scanf("%s", senha1);
    	if ((strcmp(login, login1)== 0)&&(strcmp(senha, senha1)== 0))
    		{
	    		printf("\nBem vindo Dr. Hans Chucrute");
	    		printf("\n###########################");
	    		//DADOS DAS VARIAVEIS
	    			//DADOS DAS VARIAVEIS
	    		char nome[100];
				char sobrenome[100];
				char cpf[50];
				char telefone[50];
				char rua[50];
				char numero [50];
				char bairro [50];
				char cidade [50];
				char estado [50];
				char cep [50];
				char email[50];
				char comorbidade [2];
				char diagnostico [10];
				int ano_nascimento, resultado;
				int ano =2020;
				
	    		FILE * pFile;
				printf("\n\nInforme o nome e o sobrenome do paciente: \n");
				scanf("%s""%s", &nome, &sobrenome);
				pFile = fopen(sobrenome , "a");
				if(pFile!=NULL){
				//dados do arquivo de cadastro
				printf("\nINFORME OS DADOS PARA CADASTRO:");
				printf("\nCPF:");
				scanf("%s", &cpf);
				
				printf("\ntelefone:");
				scanf("%s", &telefone);
				
				printf("\nRUA:");
				scanf("%s", &rua);
				
				printf("\nNUMERO:");
				scanf("%s", &numero);
				
				printf("\nBAIRRO:");
				scanf("%s", &bairro);
				
				printf("\nCIDADE:");
				scanf("%s", &cidade);
				
				printf("\nESTADO:");
				scanf("%s", &estado);
				
				printf("\nCEP:");
				scanf("%s", &cep);
				
				printf("\nEMAIL:");
				scanf("%s", &email);
				
				printf("\nO PACIENTE POSSUI ALGUMA COMORBIDADE?\n s P/SIM n P/NAO:");
				scanf("%s", &comorbidade);
				
				printf("\nDATA DE DIAGNOSTICO:");
				scanf("%s", &diagnostico);
				
				printf("\nANO DE NASCIMENTO:");
				scanf("%s", &ano_nascimento);
                
				fputs(nome, pFile);
                fputs(sobrenome, pFile);
                fputs(cpf, pFile);
                fputs(telefone, pFile);
                fputs(rua, pFile);
        	    fputs(numero, pFile);
                fputs(bairro, pFile);
                fputs(cidade, pFile);
                fputs(estado, pFile);
                fputs(cep, pFile);
                fputs(email, pFile);
	            fputs(comorbidade, pFile);
                fputs(diagnostico, pFile);
                fclose(pFile);
				}
				
				}else{
	    		printf("Login ou Senha invalido.");
				}
				int ano, ano_nascimento, resultado;
				scanf("%d", &ano_nascimento);
				resultado =(ano - ano_nascimento);
				printf("Idade: %d", resultado);
				if(resultado<=65){
				FILE * pFile;
				pFile = fopen("grupo_risco.txt", "a");
				scanf("%s", &cep);
				fputs(cep, pFile);
				fgets(resultado, pFile);
						}
	}

