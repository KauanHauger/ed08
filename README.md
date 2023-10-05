#include <stdio.h>
#include <stdlib.h>

void array()
{
    int n;
    printf("Digite o tamanho do array\n");
    scanf("%d", &n);
    getchar();
    while(n<0)
    {
        printf("Erro, Digite um valor positivo\n");
        scanf("%d",&n);
        getchar();
    }
    int array[n];
    for(int i=0; i<n; i++)
    {

            printf("Valor:\n");
            scanf("%d",&array[i]);
            while(array[i]<=0 || array[i]%2==0)
            {
                printf("Digite um valor impar e positivo\n");
                scanf("%d",&array[i]);
            }

    }


    printf("Valores do array\n");
    for(int i=0; i<n; i++)
    {
        printf("%d\n",array[i]);
    }
}
void mostarAray(int n,int array[], char* nomeArquivo)
{
    FILE*file=fopen(nomeArquivo,"a");
  printf("Array no arquivo\n");
  for(int i=0;i<n;i++)
  {
      printf("%d\n",array[i]);
      fprintf(file,"%d\n",array[i]);
  }
  fclose(file);


}

void array1()
{
    int n;
    char nome[100];
    printf("Digite o tamanho do array\n");
    scanf("%d",&n);
    getchar();
    int array2[n];

    for(int i=0;i<n;i++)
    {
        printf("Digite o elemento %d\n",i+1);
        scanf("%d",&array2[i]);
        while(array2[i]<0 || array2[i]%2==0)
        {
            printf("Erro numeros negativos e pares digitados tente novamente\n ");
            scanf("%d",&array2[i]);
        }
    }
    printf("Digite o nome do arquivo\n");
    scanf("%s",nome);
    mostarAray(n,array2,nome);
}

int main()
{
    int opcao;
    //int n;
    //double resultado;
    printf("Aluno: Kauan Gabriel Silva Pereira\n Matricula: 811772\n");
    printf(" Digite 0 para parar o programa\n");
    printf(" 1 para questão 1\n");
    printf(" 2 para questão 2\n");
    printf(" 3 para questão 3\n");
    printf(" 4 para questão 4\n");
    printf(" 5 para questão 5\n");
    printf(" 6 para questão 6\n");
    printf(" 7 para questão 7\n");
    printf(" 8 para questão 8\n");
    printf(" 9 para questão 9\n");
    printf(" 10 para questão 10\n");
    printf( " 11 para exercicio extra 1\n");
    printf(" 12 para exercicio extra 2\n");
    do
    {
        printf("\nEscolha sua opcao\n");
        scanf("%d",&opcao);
        getchar();
        switch(opcao)
        {
        case 1:
            array();
            break;
        case 2:
           array1();
           break;
        }

    }while(opcao!=0);
    return 0;
}

