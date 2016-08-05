# ejercicios-de-clases-y-proyectos
codigo para calcular la constante de klaperkar 
#include <stdio.h>
#include <stdlib.h>

/* run this program using the console pauser or add your own getch, system("pause") or input loop */

int main(int argc, char *argv[]) {
	
	int num,res,res2,conti=1,total,cot=0,a,b,c,d,r,i,aux;
	printf("<<<<<<<<Bienvenido>>>>>>>>> \n A continuacion vamos a demostrar si el NUMERO=?\n Es una constante de klaperkar\n");
	printf("Para CONTINUAR pulse (s) ");
	printf("salir (n)\n");
	r=tolower(getch());
	
	while(r=='s'){
		conti=1;
		cot==0;
		printf("\n\ningrese una cifra de 4 numero=  ");
		scanf("\n%d",&num);
		if(num>999){
			if(num<10000){
				if(conti==1){
					do{
						cot++;
						a=num%10;
						num=num/10;	
						b=num%10;
						num=num/10;
						c=num%10;
						d=num/10;
			
						if(a>b){
						aux=b;
						b=a;
						a=aux;
						}
						if(a>c){
						aux=c;
						c=a;
						a=aux;
						}
						if(a>d){
							aux=d;
							d=a;
							a=aux;
						}
						if(b>c){
							aux=c;
							c=b;
							b=aux;
						}
						if(b>d){
							aux=d;
							d=b;
							b=aux;
						}
						if(c>d){
							aux=d;
							d=c;
							c=aux;
							}
								
						res=(a*1000)+(b*100)+(c*10)+(d);
						res2=(d*1000)+(c*100)+(b*10)+(a);
						total=res2-res;	;
						num=total;	
						printf("\n %d   %d  = (%d) \n",res2,res,total);
						if(num==6174)	{
						conti=0;
						}
						if(num==0){
						conti=0;
						printf("\n<<<<<<<<<<nnumero regpedig>>>>>>>>>\n");
						}// 	if(res2==res)
					}//		do
					while(conti==1);
					if(num==6174){
					printf("\n\n %d  =  %d =Kaprekar.\n",cot,total);
					printf("\n  veces que se repite el proceso= %d \n",cot);
					}
				} //	if(conti==1){
			}	//if(num<10000){
		}  // if(num>999){
				
		else{
		printf("\n<<<<<<(ERROR)>>>>> \n no ingreso un numero de 4 cifras ");
		}
		
		printf("\ndesea volver a hacer el ciclo (s)");
		r=tolower(getch());
	}
	printf("\n\n\n<<<<<<<<<<<<<<HASTA PRONTO >>>>>>>>>>>>>>>> ");
	return 1;
}//echo por=kevin duran 
